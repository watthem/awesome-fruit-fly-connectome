# Awesome Fruit Fly Connectome [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources, datasets, tools, papers, visualizations, simulations, and community experiments related to *Drosophila melanogaster* (fruit fly) connectomes.

The fruit fly has become the flagship model for whole-nervous-system connectomics. Landmark releases include the larval brain (2023), the adult female brain (FlyWire, 2024), male and female ventral nerve cords, and the complete male central nervous system (MaleCNS, 2026). The September 2026 MaleCNS release (~166,700 neurons spanning brain, optic lobes, and VNC with intact neck connective) triggered a viral wave of simulations, visualizations, and playful experiments on X.

Contributions welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [Landmark Datasets](#landmark-datasets)
- [Papers & Releases](#papers--releases)
- [Tools & Viewers](#tools--viewers)
- [Analysis Libraries](#analysis-libraries)
- [Simulations & Embodied Models](#simulations--embodied-models)
- [Viral & Community Experiments](#viral--community-experiments)
- [Related Projects & Ecosystem](#related-projects--ecosystem)
- [Learning Resources](#learning-resources)

## Landmark Datasets

- **[MaleCNS](http://male-cns.janelia.org/)** - First complete connectome of an adult male fly central nervous system: brain, optic lobes, and ventral nerve cord (~166,700 neurons, ~125 million synapses), released 2026. Enables full sensory-to-motor tracing and sexual dimorphism comparisons. [ [downloads](http://male-cns.janelia.org/download/) ]
- **[FlyWire / FAFB](https://flywire.ai)** - First complete adult female fly brain connectome, released 2024 (~139,000-140,000 neurons, >50 million synapses). [ [explorer](https://codex.flywire.ai) ]
- **Hemibrain** - Partial adult female central brain (~25,000 neurons), released 2020. Foundational earlier map from Janelia FlyEM.
- **Larval Brain Connectome** - Complete synaptic-resolution map of the *Drosophila* larva brain (~3,016 neurons, ~548,000 synapses), released 2023.
- **VNC Connectomes (MANC / FANC)** - Male Adult Nerve Cord and Female Adult Nerve Cord connectomes. Critical for motor control studies.
- **BANC** - Brain And Nerve Cord: a female whole-CNS connectome effort.

See also the comparative table in [flyconnecto.me](https://flyconnecto.me)'s "The Adult Drosophila Connectome Ecosystem."

## Papers & Releases

### Core MaleCNS Papers (2026)

- **Sexual dimorphism in the complete *Drosophila* male central nervous system connectome** - Berg, Beckett, Costa, Schlegel, Januszewski, Marin, et al. (Jefferis lab), *Cell*, 2026. The primary MaleCNS paper; identifies sex-specific and dimorphic cell types (~4.8% of central brain).
- Companion papers on visual pathways, taste, and social behavior released alongside the main MaleCNS resource.
- [A connectomics milestone: Mapping the complete male fruit fly brain](https://research.google/blog/a-connectomics-milestone-mapping-the-complete-male-fruit-fly-brain/) - Google Research blog.
- Janelia / HHMI / MRC LMB / Cambridge announcements (Sept 2026).

### FlyWire / Adult Female Brain (2024)

- **Neuronal wiring diagram of an adult brain** - Dorkenwald et al. / FlyWire Consortium, *Nature*, 2024.
- **Whole-brain annotation and multi-connectome cell typing of *Drosophila*** - Schlegel et al., *Nature*, 2024. Hierarchical cell types and a consensus atlas.
- **Network statistics of the whole-brain connectome of *Drosophila*** - *Nature*, 2024.
- A package of nine *Nature* papers (Oct 2024) demonstrating circuit discoveries from this release.

### Earlier Milestones

- **The connectome of an insect brain** (larval brain) - Winding et al., *Science*, 2023.
- Hemibrain - Scheffer et al., *eLife*, 2020.
- Male VNC (MANC) - Takemura et al., *eLife*, 2024, and related female VNC work.

## Tools & Viewers

- **[Codex](https://codex.flywire.ai)** - Primary interactive portal for FlyWire: search neurons, view connectivity, snapshots, and networks.
- **[neuPrint](https://neuprint.janelia.org)** - Queryable database used for hemibrain, MANC, MaleCNS, and other datasets.
- **Neuroglancer** - High-performance web-based 3D volume and segmentation viewer, widely used across datasets.
- **Clio** - Annotation-focused viewer for MaleCNS and related data.
- **Male CNS Cell Type Explorer** and **Dimorphism Explorer** - Dedicated tools on the MaleCNS project page.
- **NeuronBridge** - Matches neurons across datasets, including MaleCNS.
- **[braincircuits.io](https://braincircuits.io)** - Additional analysis and visualization front-end.
- CATMAID-based project instances - Collaborative annotation and proofreading, used historically across several fly datasets.
- **FlyWire Proofreading interface** - Collaborative proofreading platform (historical and ongoing).

## Analysis Libraries

### Python

- **navis** + **navis-flybrains** - Morphology analysis, visualization, and template transforms.
- **fafbseg-py** - FlyWire / FAFB-specific tools.
- **CAVEclient** - Access to CAVE-hosted datasets (FlyWire, etc.).
- **neuprint-python** - Query neuPrint databases (hemibrain, MANC, MaleCNS, ...).
- **cocoa** - Comparative connectomics.
- CloudVolume / skeletor for meshes and volumes.

### R (natverse ecosystem)

- **natverse**, **neuprintr**, **fafbseg**, **hemibrainr**, **malevnc**, **malecns**, **bancr**, **coconat** / **coconatfly**.

Many GitHub tutorials exist (e.g., seung-lab/FlyConnectome, sjcabs/fly_connectome_data_tutorial, flyconnectome org repositories).

## Simulations & Embodied Models

- **NeuroMechFly** - Data-driven neuromechanical model of adult *Drosophila* (v1 and v2) combining biomechanics, muscles, and neural controllers in a physics simulator; supports vision, olfaction, complex terrain, and connectome-constrained circuits. Papers in *Nature Methods* (2022 & 2024).

Community simulations using the open MaleCNS / FlyWire data (often with leaky-integrate-and-fire or RL fine-tuning) have exploded since the 2026 release.

## Viral & Community Experiments

The MaleCNS release (especially Sept 2026) sparked a creative wave on X. Verified examples:

- Simulated MaleCNS controlling agents in **Minecraft**, **Beat Saber**, **Mario 64**, and **Doom** ("DOOMFLY") - widely reported across independent outlets. [ [PC Gamer](https://www.pcgamer.com/hardware/after-google-mapped-an-adult-male-fruit-flys-brain-software-engineers-made-it-play-doom-mario64-and-beat-saber/) | [Dexerto](https://www.dexerto.com/gaming/googles-digital-fly-brain-gets-its-own-heaven-after-going-through-beat-saber-hell-3407304/) ]
- **Stonkfly** - A simulated fly connectome given real money to trade BTC-USDC on Coinbase, with trades tied to simulated dopamine-neuron activity. [ [repo](https://github.com/nftechie/stonkfly) ]
- An NFT collection at flynft.online driven by simulated walking/cursor control - a real, on-theme experiment, but also an active crypto/NFT storefront tied to a token; link at your own discretion rather than treating it as a neutral demo.
- The sexual-dimorphism and courtship-circuit findings from the MaleCNS papers drew significant community discussion, though no interactive "courtship circuit" demo (analogous to the game/trading demos above) was found.

These are typically topology-inspired neural networks or simplified dynamical simulations of the published wiring diagram, not literal biological tissue. A few claims that circulated with this wave — including a "driving cars" demo and the claim that the fly brain "only wanted to talk about rotten fruit" — rest on thin or single-source evidence and should not be repeated as confirmed.

Search X for recent posts combining "MaleCNS", "fruit fly connectome", "FlyWire", or specific demos for the latest wave.

## Related Projects & Ecosystem

- **Janelia FlyEM Project Team** - Core producers of many EM volumes and connectomes.
- **FlyWire Consortium** (Princeton + global collaborators) - Crowdsourced proofreading and annotation.
- **Cambridge Connectomics Group** / MRC LMB (Jefferis lab) - Major annotation and comparative work.
- **Google Research** - AI/ML contributions to reconstruction and scale.
- Ongoing vertebrate efforts (larval zebrafish, *Danionella*, mouse) building on fly lessons.
- Comparative resources and multi-connectome cell typing pipelines.

## Learning Resources

- FlyWire-related educational materials and blogs (Google Research, Janelia, HHMI, MRC LMB, Princeton Neuroscience Institute).
- *Nature* / *Cell* / *Science* news & views accompanying major releases.
- YouTube / project videos of cell-type galleries and example pathways.
- GitHub tutorial repositories for getting started with data access and analysis.

---

## Footnotes

License: this list's structure is dedicated to the public domain under [CC0](LICENSE). Individual resources retain their own original licenses — notably, **MaleCNS data is CC BY 4.0** (permissive, attribution required, commercial use fine), while **FlyWire/FAFB data is CC BY-NC 4.0** (non-commercial use only). Check each dataset's own terms before reuse; do not assume all listed data shares the same license.

*Last major update: September 2026, timed with the MaleCNS viral wave. Fly on! 🪰*
