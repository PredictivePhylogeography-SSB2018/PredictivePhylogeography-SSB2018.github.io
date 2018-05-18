---
title: Selected readings
description: Readings about models to be used and key systems
header: Selected readings
---

Below we summarize and categorize some key papers relevant to our working group.

Theories of assembly and diversification
========================================

Core ecological neutrality
--------------------------

**S. P. Hubbell (2001):** The book on the matter.

**Etienne (2005):** A backward in time ("ancestry assignment") algorithm for the simple neutral theory. But inherently it produces phylogenies, and possibly geneologies on which mutations could be introduced.

**Alonso and McKane (2004):** A forward time sampling theory for Hubbell's model.

**Etienne, Alonso, and McKane (2007):** Explores whether the zero-sum assumption of Hubbell's original model is neccesary and concludes that it's not.

**Rosindell et al. (2012):** After 10+ years of study on Hubbell's model, this lays at the case in favor of what that model offers

Core sampling formulae
----------------------

These approaches use master equations (or a related approach) of the assembly dynamics to derive equations for the population sizes of species. Not all approaches are inherently neutral

**Kendall (1948):** Derives the sampling distribution for a birth-death-immigration process---which is precisely the process we care about when considering the assembly of a local community.

**Haegeman and Etienne (2017):** A fantastic paper about sampling distributions under a variety of scenarios. Inspired by much of the work discussed below on sampling the neutral theory of biodiversity.

Core statistical mechanical theories/models of assembly
-------------------------------------------------------

**Pueyo (2006):** Overview of the philosophy and potential for the principle of maximum information entropy applied to ecology

**Banavar, Maritan, and Volkov (2010):** A nice review of MaxEnt, with many examples from ecology

**J Harte et al. (2008):** Lays the foundation for John's MaxEnt theory of abundances, metabolic rates, and spatial distributions

**John Harte, Smith, and Storch (2009):** Extends J Harte et al. (2008) to look explicitly at spatial scaling.

**Bowler and Kelly (2012):** A nice application of MaxEnt to derive (using a very different approach from John) the Fisher log-series.

Spatially explicit neutral ecology
----------------------------------

**Rosindell, Wong, and Etienne (2008):** An algorithm is presented to simulate spatially-explicity neutral communities in a study plot embedded within an infinite landscape. The algorithm is backward in time (i.e. coalescent) providing computational efficiences, further added by clever indexing. It should be noted that the coalescent algorithm they present can only provide simulated communities in equilibrium because the coalesences in allowed to occur over potentially infinite time. This algorithm is used in Rosindell and Cornell (2007) to study the SAR.

**O’Dwyer and Cornell (2017):** Spatially explicit backward time model with analytical results. Effectively Rosindell, Wong, and Etienne (2008) but with an approximate analytical solution.

**Etienne and Rosindell (2011):** Uses Rosindell, Wong, and Etienne (2008) to simulate spatially explicit lanscapes, but then fits classic spatially implicity neutral theory to those. Shows that the results are not consistent, and that spatially implicit theory does a better job matching real data. Suggests that perhaps field theory models (e.g spatailly implicit neutral theory) do better because they average over many details that explicit models must get exactly right

**Rosindell and Cornell (2013):** Again uses Rosindell, Wong, and Etienne (2008) to show that Fisher log-series shows up at small and largest scales. This brings spatially explicit neutral SAD back in better agreement with data, also provides oppurtunities to more rigorously test neutral theory.

**O’Dwyer and Green (2010):** Cool paper, but the field-theoretic approach is not correct, as shown by our own Grilli et al. (2012).

Island neutral ecology models
-----------------------------

**Etienne (2007):** Provides an analytical solution to sampling formula for multiple samples from the same metacommunity. Also provides an algorithm (seemingly backword in time) for generating such samples. This algorithm could be a very good jumping off point for simulating multiple islands. Immigration between islands would need to be added. The algorithm seems to be vectorizable too.

**Rosindell and Phillimore (2011):** The model for neutral island community evolution. Options for different speciation mechanisms including protracted.

**Rosindell and Harmon (2013):** Model of community assembly on islands with immigration only

More thoughts on speciation and phylogenies in neutral ecology models
---------------------------------------------------------------------

**Rosindell et al. (2010):** The protracted speciation model. Backward in time simulation. The model retains much of the positive traits of classic neutral theory (e.g. Fisher log series) but has more realistic dynamics.

**Rosindell and Phillimore (2011):** Extension of the protracted speciation model to include anagenesis/cladogenesis, and immigration rate proportional to island size.

**Etienne and Haegeman (2011):** A different model for more realistic speciation in which species randomly split into new species. Does a worse job (but not by much) of fitting the SAD, and the metacommunity SAD becomes broken stick instead of Fisher---could be a good thing or a bad thing. But the deep time dynamics (i.e. speciation events) are more realistic. No backward time simulation is possible because random fission is not a reversible process.

**Jabot and Chave (2009):** Uses Etienne (2005) simulation method to do ABC on phylogenies and abundance data. Shows that phylogenetic balance helps parameter identifiability.

Non-neutral ecology models
--------------------------

**Rosindell, Harmon, and Etienne (2015):** Basically the same model as Kessler and Shnerb (2014) but assuming brownian motion of fitness instead of fitness evolving on a quadratic fitness landscape. Forward time simulation implemented.

**Kessler and Shnerb (2014):** Provides several models, but most usefully a forward time simulation of all the dynamics of neutral theory plus heiritable differences in fitness. Could be useful for thinking about environmentally explicit models. No code or pseudo code provided.

**Carmel et al. (2017):** Re-dirivation of the fitness difference vs. niche difference framework, but with rigorous mathematics. Could be a useful model for simulating species interactions but the paper itself dosen't present a simulation, only analytical results.

Model fitting and inference
===========================

**B. McGill (2003)** **B. J. McGill et al. (2007)**

Key systems
===========

Coalescent models
=================

References
----------

Alonso, David, and Alan J McKane. 2004. “Sampling Hubbell’s Neutral Theory of Biodiversity.” *Ecol. Lett.* 7 (10): 901–10.

Banavar, Jayanth R, Amos Maritan, and Igor Volkov. 2010. “Applications of the Principle of Maximum Entropy: From Physics to Ecology.” *J. Phys. Condens. Matter* 22 (6): 063101.

Bowler, Michael G, and Colleen K Kelly. 2012. “On the Statistical Mechanics of Species Abundance Distributions.” *Theor. Popul. Biol.* 82 (2): 85–91.

Carmel, Yohay, Yevhen F Suprunenko, William E Kunin, Rafi Kent, Jonathan Belmaker, Avi Bar-Massada, and Stephen J Cornell. 2017. “Using Exclusion Rate to Unify Niche and Neutral Perspectives on Coexistence.” *Oikos* 126 (10). Blackwell Publishing Ltd: 1451–8.

Etienne, Rampal S. 2005. “A New Sampling Formula for Neutral Biodiversity.” *Ecol. Lett.* 8 (3). Blackwell Science Ltd: 253–60.

———. 2007. “A Neutral Sampling Formula for Multiple Samples and an ’Exact’ Test of Neutrality.” *Ecology Letters* 10: 608–18.

Etienne, Rampal S, David Alonso, and Alan J McKane. 2007. “The Zero-Sum Assumption in Neutral Biodiversity Theory.” *J. Theor. Biol.* 248 (3): 522–36.

Etienne, Rampal S, and Bart Haegeman. 2011. “The Neutral Theory of Biodiversity with Random Fission Speciation.” *Theor. Ecol.* 4 (1): 87–109.

Etienne, Rampal S, and James Rosindell. 2011. “The Spatial Limitations of Current Neutral Models of Biodiversity.” *PLoS One* 6 (3): e14717.

Grilli, Jacopo, Sandro Azaele, Jayanth R Banavar, and Amos Maritan. 2012. “Absence of Detailed Balance in Ecology\[No Title\].” *EPL* 100: 38002.

Haegeman, Bart, and Rampal S Etienne. 2017. “A General Sampling Formula for Community Structure Data.” *Methods Ecol. Evol.*

Harte, J, T Zillio, E Conlisk, and AB Smith. 2008. “Maximum entropy and the state-variable approach to macroecology.” *Ecology* 89 (10): 2700–2711.

Harte, John, Adam B Smith, and David Storch. 2009. “Biodiversity scales from plots to biomes with a universal species-area curve.” *Ecology Letters* 12 (8): 789–97.

Hubbell, S. P. 2001. *The Unified Neutral Theory of Biodiversity and Biogeography*. Princeton University Press.

Jabot, Franck, and Jérôme Chave. 2009. “Inferring the Parameters of the Neutral Theory of Biodiversity Using Phylogenetic Information and Implications for Tropical Forests.” *Ecol. Lett.* 12 (3). Blackwell Publishing Ltd: 239–48.

Kendall, David G. 1948. “On Some Modes of Population Growth Leading to R. a. Fisher’s Logarithmic Series Distribution.” *Biometrika* 35 (1): 6–15.

Kessler, David A, and Nadav M Shnerb. 2014. “Neutral-Like Abundance Distributions in the Presence of Selection in a Continuous Fitness Landscape.” *J. Theor. Biol.* 345 (March): 1–11.

McGill, B. 2003. “Strong and Weak Tests of Macroecological Theory.” *Oikos* 102 (3). Munksgaard International Publishers: 679–85.

McGill, Brian J, Rampal S Etienne, John S Gray, David Alonso, Marti J Anderson, Habtamu Kassa Benecha, Maria Dornelas, et al. 2007. “Species Abundance Distributions: Moving Beyond Single Prediction Theories to Integration Within an Ecological Framework.” *Ecol. Lett.* 10 (10): 995–1015.

O’Dwyer, James P, and Stephen J Cornell. 2017. “Cross-Scale Neutral Ecology and the Maintenance of Biodiversity,” May.

O’Dwyer, James P, and Jessica L Green. 2010. “Field Theory for Biogeography: A Spatially Explicit Model for Predicting Patterns of Biodiversity.” *Ecol. Lett.* 13 (1): 87–95.

Pueyo, Salvador. 2006. “Diversity: Between Neutrality and Structure.” *Oikos* 112 (2). Munksgaard International Publishers: 392–405.

Rosindell, James, and Stephen J Cornell. 2007. “Species-Area Relationships from a Spatially Explicit Neutral Model in an Infinite Landscape.” *Ecol. Lett.* 10 (7): 586–95.

———. 2013. “Universal Scaling of Species-Abundance Distributions Across Multiple Scales.” *Oikos* 122 (7). Blackwell Publishing Ltd: 1101–11.

Rosindell, James, and Luke J Harmon. 2013. “A Unified Model of Species Immigration, Extinction and Abundance on Islands.” Edited by K C Burns. *J. Biogeogr.* 40 (6): 1107–18.

Rosindell, James, and Albert B Phillimore. 2011. “A Unified Model of Island Biogeography Sheds Light on the Zone of Radiation.” *Ecol. Lett.* 14 (6). Blackwell Publishing Ltd: 552–60.

Rosindell, James, Stephen J Cornell, Stephen P Hubbell, and Rampal S Etienne. 2010. “Protracted Speciation Revitalizes the Neutral Theory of Biodiversity.” *Ecol. Lett.* 13 (6): 716–27.

Rosindell, James, Luke J Harmon, and Rampal S Etienne. 2015. “Unifying Ecology and Macroevolution with Individual-Based Theory.” Edited by Arne Mooers. *Ecol. Lett.* 18 (5): 472–82.

Rosindell, James, Stephen P Hubbell, Fangliang He, Luke J Harmon, and Rampal S Etienne. 2012. “The Case for Ecological Neutral Theory.” *Trends Ecol. Evol.* 27 (4): 203–8.

Rosindell, James, Yan Wong, and Rampal S Etienne. 2008. “A Coalescence Approach to Spatial Neutral Ecology.” *Ecol. Inform.* 3 (3): 259–71.
