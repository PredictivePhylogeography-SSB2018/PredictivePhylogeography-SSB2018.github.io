**Why are there so many different kinds of markdown!?!?!?!?! Aghhhghhhhhrrrhhhh!**

>20  * How does system size (and isolation) determine community assembly on evolutionary timescales?

>15  * What are the mechanisms that drive radiations?

>15  * What is the effect of habitat dynamics (e.g. island ontogeny) in determining present-day biodiversity patterns?

>10  * What determines resistance to invasion?

>14  * Where is the diversity emerging, at the alpha level or at the beta level? Corrolary: Where do novel ecotypes come from? From evolution or dispersal?

>5   * Does speciation fill niche space or create niches; does diversity beget diversity?

>7   * Are commonness and rarity persistent across space and time?

>4   * How does abundance partition into different clades? Does a clade's richness in a community correlate with the overall richness of the community?

>5   * What are the limits to species richness?

>6   * Are there limits to predictability of ecosystems (how much is truly stochastic)?

>6   * What's the role of speciation in modifying networks?

### Habitat Dynamics/Island Ontogeny
* Varying J
* Splitting the island into multiple habitats
    * Habitats each have independent J
    * J will vary with time (upper habitats will become smaller as the islands erode).
    * Essentiallly adding more linked habitats to the model
        * Galapagos (finches will see the islands as a hole, and snails will see independent environments).
* What does the data you need to test this look like?
* Do we really need a multiple J model? Could a changing J explain the data just as much?

### Alpha/Beta Group
* Patterns of alpha/beta/gamma. Richness + Area plot; gamma diversity.
* Add a phylogeny, endemics, and multiple island species, measure relative importance of diversification and colonization.
* Diversification rates as a function of abundance, could be a quick win (even though nobody voted for it).
    * Do common or rare species speciate more? (Putting abundance data together with the phylogeny).
* Scaling relation
* Beta diversity needs spatial scale (two patches is fine), spatially implicit is fine.
* We need speciation happening local and regional.
    * Don't feel like popgen data is necessary, but abundance data and phylogenies could still make a whole lot of cool stuff happen.
* Traits and functional diversity (replace taxonomic diversity questions above with functional diversity).

### Diversification scaling
* CNEAT Model
    * C(lades), N(abundance), E(nvironment), A(rea), T(ime) - The 'C' is silent.
* Phylogeneticists think about rates on a phylogeny (it's a property of the tree), ecologists have speciation as a property of the local community.
* Scale of space and time you consider and how abundance drives speciation and extinction.
    * Things with high abundance disperse more and wash out speciation.
    * Environmental heterogeneity between patches (interaction between abundance and diversification rate)
* Joint phylogeny and community data can be used to fit the data (and estimate rates?)
* Abundance could fluctuate through time and space, have 2 knobs to tweak: mean and variance of abundance through space.
    * Decreased variance in abundance could be a density dependence thing.

* (see james' zones of radiation thing)
* Speciation rate depends on the number of individuals in the Hubbel model, but here all trees look like they may be slowing down in time.
    * Zero sum thing is important for constraining global # of lineages.

* Interests: Purely empirical looking at plots of abundance vs branch lengths
* North american breeding birds (have abundances, and a nice tree, and occurrences for environmental heterogeneity).
    * Partition by guild, and look at rates w/in guilds? Maybe rates are explained just by abundance of clades?
* Pure simulation model to look at what positive correlation between speciation and abundance
* **The Petr-Andy Lunch Line Model**
* Do parameters imply positive or negative relationship between measures of "scale" and diversification rate?

### Radiations
* Minimal model to answer questions about radiations and dispersal (why do some things radiate and some things not)?
* Model should inculde multiple immigration event from the source to at least 2 islands
    * Later immigrations may end up radiating
    * Niche filling could inhibit radiation
* Simulations and Data are needed
* Key ingredients:
    * Differences in environment or resources
    * Some kind of niches
    * Isolation/patches
* Individual based or species based or some kind of "hack"
    * Complexity vs tractability
* Three possible models to implement this in
    * DMI incompatibility model with environment added
    * Adaptive dynamics
    * MESS
* Spatially should be patch based and discrete, but continuousity of environment is undecided.
* Diversification between niches w/in an environment vs between environments
    * Almost immediate co-occurrences, the radiation forms quickly (sister taxa diverging between resources w/in an environment)
    * Divergence between habitats adapts to different kinds of environments so it looks like allopatry.
    * The key difference is separation in space.
**In my mind you're either gravel or you're a boulder.**

