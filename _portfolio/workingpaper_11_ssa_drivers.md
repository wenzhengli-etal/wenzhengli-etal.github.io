---
title: "What explains urban spatial structure in Sub-Saharan African cities? Markets, infrastructure, and institutions"
collection: portfolio
order: 5
status: "In progress"
authors: "Wenzheng Li, Stephan Schmidt"
image: "/images/SSA_corridors.jpg"
summary: "Why do some African cities grow a second center while others simply spread? Testing market forces, street supply, and local government structure against four measures of urban form across 482 cities &mdash; and finding that road-rich cities do not get more centers, but a more substantial second one."
---

Having traced how urban structure changed, this paper asks what accounts for it. Each of four outcomes — whether a city is polycentric, how many centers it has, how balanced its two largest centers are, and how much of the population lives outside the centers — is regressed on the same set of variables, grouped by the three families of explanation in the literature, with five geography controls in every model. Each outcome is estimated twice: without fixed effects, where country-level variables are identified, and with country fixed effects, where the remaining coefficients come from differences between cities of the same country.

**Market forces** enter as city population and household wealth. City size is the first-order determinant of urban structure in theory, and the wealth index stands for the demand side of the housing market: informal fringe growth is the response of poor households to unaffordable serviced land. **Infrastructure** enters as street length per resident — the supply of network that lets a city spread and lets secondary centers form. **Politics and institutions** enter as the number of general-purpose local governments per 10,000 residents (the fragmentation measure of the sprawl literature), a dummy for a two-tier authority covering the whole footprint, and a dummy for French administrative legacy.

<figure class="wl-figure">
  <img src="/images/SSA_drivers_coefficients.jpg" alt="Coefficient plot with confidence intervals for four outcomes: polycentric, number of centers, polycentricity and dispersion.">
  <figcaption>Standardized coefficients for the four outcomes with 95% confidence intervals, estimated with and without country fixed effects.</figcaption>
</figure>

Population is the strongest regressor throughout: larger cities have more centers, are more likely to be polycentric, have a more balanced pair of leading centers, and are more dispersed. Street supply works differently from what a simple reading would predict. With country fixed effects, one more standard deviation of street length per capita raises the probability that a city is polycentric and raises both CP and DISP, but its effect on the *number* of centers is significant only without fixed effects. Road-rich cities therefore do not have more centers; their second center is more substantial, and their population is spread more widely. Street supply shapes the form of the city rather than the count of its centers.

On the institutional side, fragmentation and coordination pull in opposite directions: more local governments per capita is associated with more centers and more dispersion, while a two-tier authority covering the whole footprint is associated with fewer centers and a more compact city on all four outcomes. What matters most, though, is how the two combine.

Interacting fragmentation with the two-tier dummy sharpens the picture. In cities *without* a city-wide authority, one more standard deviation of fragmentation raises dispersion by +0.038\*\*\* and the log number of centers by +0.119\*\*\*. In two-tier cities the dispersion slope falls to &minus;0.018 and is no longer significant, while the centers slope rises to +0.344\*\*\*. The consistent reading is that a city-wide government holds the city together: when many basic-level governments sit underneath it, each grows its own small subcenter within that envelope, so the people who leave the main center cluster into centers rather than spreading out. Without such an authority the same number of governments produces outward spread and only slightly more centers. A two-tier system therefore does not create polycentricity — the near-zero interaction for CP (+0.007) says the additional centers are small and the dominance of the main center is unchanged — it channels the consequences of fragmentation from sprawl into organized subcenters.

French colonial legacy works the same way. In French-legacy cities fragmentation brings more, smaller centers (+0.276\*\*\* against +0.107\*\*\* per standard deviation) and no additional dispersion (+0.008 against +0.041\*\*\*), while the polycentric dummy and CP are unaffected. The main effect, in the models without fixed effects, is negative on all four outcomes — the finding of Baruah, Henderson and Peng (2021) that Francophone cities are more compact and more monocentric. The mechanism is plausible: French rule left a top-down system of urban management in which communes are basic units under the tutelage of the state, and the large cities are organized as a *ville* or *communauté urbaine* subdivided into *communes d'arrondissement*. Many basic units then mean many internal districts, each with its own small center, while the growth of the city as a whole remains managed from above.

Three strands of supplementary evidence carry what the regressions cannot. On informality, street-block complexity from the Million Neighborhoods database shows that informality by street access is spread over the whole city rather than concentrated in its centers, and that subcenters which emerged after 2004 start out more informal than those already present. On infrastructure, the subcenters of many cities are strung along a single road corridor, and in several cases the road is visibly there before the subcenters are.

<figure class="wl-figure">
  <img src="/images/SSA_corridors.jpg" alt="Six city maps showing main centers, numbered subcenters and the road corridor carrying most of them.">
  <figcaption>Subcenters strung along one road corridor, 2024: Hawassa, Addis Ababa, Kigali, Sokoto, Mbeya and Johannesburg. Red is the main center, blue the numbered subcenters, orange the corridor carrying most of them.</figcaption>
</figure>
