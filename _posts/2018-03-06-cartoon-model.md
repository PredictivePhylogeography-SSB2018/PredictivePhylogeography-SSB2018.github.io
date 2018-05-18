---
title: The messDiv model
description: Cartoon version of the model
header: Cartoon model
---
The model as of right now works as follows.

![Schematic of regional pool and local community processes.]({{ site.baseurl }}/img/fig_mod.jpg)

1. Simulate a phylogenetic tree under a speciation-extinction model with birth rate $\lambda$ and death rate $c\lambda$ where $c$ determines the proportion of extinction relative to speciation and is bounded between 0 and 1.
2. Simulate species' traits under a Brownian motion model with parameters starting value $\theta$ and variance $\sigma^2$.
3. Draw abundances from a logseries distribution and randomly assign them to tips on the tree. *This is now the mainland species pool.*
4. We now prepopulate the island community with a starting community. This can be done in two ways, volcanic or landbridge, as follows.

    In the volcanic scenario, the island is first filled with "empty niche" individuals who take up space that will later be occupied by real individuals.

    We then choose one individual from the most abundant species on the mainland. This individual colonizes the island.

    When deaths occur, the "empty niche" individuals die at the same rate as normal indivduals, but can't give birth. So, they are eventually replaced by real simulated creatures.

    For the landbridge scenario, individuals are chosen at random from the mainland pool until the local community is full. The simulation then begins from this randomly selected community.
5. The simulation is now run as follows: for each time step, one individuals dies in the island community. The individual that dies is either random (neutral case) or depends on either competition or environmental filtering.
    
    Under *environmental filtering*, each individual has a relative chance of death that depends on how different its trait ($z_i$) is from the environmental optimum ($\theta$):

    <div>
    $$
    p_i = e^{\frac{(z_i - z_{opt})^2}{w^2_{hf}}}
    $$
    </div>

    $z_{opt}$ is itself a free parameter which determines the environment for the island. $w_{hf}$ determines how strong environmental filtering is: larger $w_{hf}$ values lead to less filtering. In the limit of $w_{hf} \rightarrow \infty$ the local community is neutral.
    
    Under *competition*, each individual has a relative chance of death that depends on how different its trait ($z_i$) is from the other individuals in the community ($z_j$):

    <div>
    $$
    p_i = 1 - e^{\frac{\frac{1}{N}\sum_{j}(z_i - z_j)^2}{w^2_{c}}}
    $$
    </div>

    $w_c$ determines the niche width over which competition occurs between individuals---the larger $w_c$, the stronger competition, even between individuals with vastly different traits. In the limit of $w_c \rightarrow \infty$ the local community is neutral.

6. Deaths are then replaced by either births from within the island (with probability $1-\nu$) or migrants from the mainland (with probability $\nu$). If birth, then we randomly select an individual to give birth from the local community, with each individual equally likely to be chosen. If migrant, the individual is randomly selected from the mainland pool.

7. Steps 4 and 5 are repeated a large number of times until the simulation reaches equilibrium. We use the test suggested by Rosindell and Harmon where equilibrium is reached once there are no longer any descendants of the founders on the island.

8. Now we use a coalescent approach to simulate genetic diversity data for the species on the island. For each species on the island, we use its current population size, number of colonization events, and the time it first colonized the island to parameterize a coalescent model with mutation rate $\mu$. We assume either that the species immediately grew to their current size just after colonization and were constant until the present day, or that they grew exponentially from one individual to their current population size.
