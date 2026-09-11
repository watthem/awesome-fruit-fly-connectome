# Awesome Fruit Fly Connectome 🪰🧠

> A curated list of resources, datasets, tools, papers, visualizations, simulations, and community experiments related to *Drosophila melanogaster* (fruit fly) connectomes.

The fruit fly has become the flagship model for whole-nervous-system connectomics. Landmark releases include the larval brain (2023), the adult female brain (FlyWire, 2024), male and female ventral nerve cords, and the complete male central nervous system (MaleCNS, 2026). The September 2026 MaleCNS release (~166,700 neurons spanning brain + optic lobes + VNC with intact neck connective) triggered a viral wave of simulations, visualizations, and playful experiments on X.

Inspired by the [awesome](https://github.com/sindresorhus/awesome) lists. Contributions welcome (especially from local CLI bots and community researchers)!

## Contents

- [Landmark Datasets](#landmark-datasets)
- [Papers & Releases](#papers--releases)
- [Tools & Viewers](#tools--viewers)
- [Analysis Libraries](#analysis-libraries)
- [Simulations & Embodied Models](#simulations--embodied-models)
- [Viral & Community Experiments](#viral--community-experiments)
- [Related Projects & Ecosystem](#related-projects--ecosystem)
- [Learning Resources](#learning-resources)
- [Contributing](#contributing)

## Landmark Datasets

- **MaleCNS (Male Central Nervous System, 2026)** — First complete connectome of an adult male fly CNS: brain + optic lobes + VNC (~166,700 neurons, ~125 million synapses). Enables full sensory-to-motor tracing and sexual dimorphism comparisons.  
  Official site: [male-cns.janelia.org](http://male-cns.janelia.org/)  
  neuPrint / downloads available via Janelia FlyEM.

- **FlyWire / FAFB (Full Adult Fly Brain, 2024)** — First complete adult female brain connectome (~139,000–140,000 neurons, >50 million synapses).  
  [flywire.ai](https://flywire.ai) · Codex explorer · Public data downloads.

- **Hemibrain (2020)** — Partial adult female central brain (~25,000 neurons). Foundational earlier map from Janelia FlyEM.

- **Larval Brain Connectome (2023)** — Complete synaptic-resolution map of the *Drosophila* larva brain (~3,016 neurons, ~548,000 synapses).

- **VNC Connectomes** — Male Adult Nerve Cord (MANC) and Female Adult Nerve Cord (FANC). Critical for motor control studies.

- **BANC** — Brain And Nerve Cord (female whole CNS efforts).

See also the comparative table in “The Adult Drosophila Connectome Ecosystem” (flyconnecto.me).

## Papers & Releases

### Core MaleCNS Papers (2026)
- **Sexual dimorphism in the complete *Drosophila* male central nervous system connectome** (Berg, Beckett, Costa, Schlegel, Januszewski, Marin, … Jefferis et al., *Cell*, 2026). Primary MaleCNS paper. Identifies sex-specific and dimorphic cell types (~4.8% of central brain).
- Companion papers on visual pathways, taste, and social behavior released alongside the main MaleCNS resource.
- Google Research blog: [A connectomics milestone: Mapping the complete male fruit fly brain](https://research.google/blog/a-connectomics-milestone-mapping-the-complete-male-fruit-fly-brain/).
- Janelia / HHMI / MRC LMB / Cambridge announcements (Sept 2026).

### FlyWire / Adult Female Brain (2024)
- **Neuronal wiring diagram of an adult brain** (Dorkenwald et al. / FlyWire Consortium, *Nature*, 2024).
- **Whole-brain annotation and multi-connectome cell typing of *Drosophila*** (Schlegel et al., *Nature*, 2024) — Hierarchical cell types and consensus atlas.
- **Network statistics of the whole-brain connectome of *Drosophila*** (*Nature*, 2024).
- Package of nine *Nature* papers (Oct 2024) demonstrating circuit discoveries.

### Earlier Milestones
- Larval brain connectome (Winding et al., *Science*, 2023).
- Hemibrain (Scheffer et al., 2020).
- Male VNC (Takemura et al., *eLife*, 2024) and related female VNC work.

## Tools & Viewers

- **Codex (Connectome Data Explorer)** — Primary interactive portal for FlyWire: search neurons, view connectivity, snapshots, networks. [codex.flywire.ai](https://codex.flywire.ai)
- **neuPrint** — Queryable database used for hemibrain, MANC, MaleCNS, etc. [neuprint.janelia.org](https://neuprint.janelia.org)
- **Neuroglancer** — High-performance web-based 3D volume & segmentation viewer (widely used across datasets).
- **Clio** — Annotation-focused viewer for MaleCNS and related data.
- **Male CNS Cell Type Explorer** & **Dimorphism Explorer** — Dedicated tools on the MaleCNS project page.
- **NeuronBridge** — Matches across datasets (including MaleCNS support).
- **CATMAID Spaces** & **braincircuits.io** — Additional analysis and visualization front-ends.
- **FlyWire Proofreading interface** — Collaborative proofreading platform (historical and ongoing).

## Analysis Libraries

### Python
- **navis** + **navis-flybrains** — Morphology analysis, visualization, template transforms.
- **fafbseg-py** — FlyWire / FAFB-specific tools.
- **CAVEclient** — Access to CAVE-hosted datasets (FlyWire, etc.).
- **neuprint-python** — Query neuPrint databases (hemibrain, MANC, MaleCNS…).
- **cocoa** — Comparative connectomics.
- CloudVolume / skeletor for meshes and volumes.

### R (natverse ecosystem)
- **natverse**, **neuprintr**, **fafbseg**, **hemibrainr**, **malevnc**, **malecns**, **bancr**, **coconat** / **coconatfly**.

Many GitHub tutorials exist (e.g., seung-lab/FlyConnectome, sjcabs/fly_connectome_data_tutorial, flyconnectome org repositories).

## Simulations & Embodied Models

- **NeuroMechFly** (v1 and v2) — Data-driven neuromechanical model of adult *Drosophila* combining biomechanics, muscles, and neural controllers in a physics simulator. Supports vision, olfaction, complex terrain, and connectome-constrained circuits.  
  Papers in *Nature Methods* (2022 & 2024). Excellent for testing sensorimotor hypotheses.

Community simulations using the open MaleCNS / FlyWire data (often with leaky-integrate-and-fire or RL fine-tuning) have exploded since the 2026 release.

## Viral & Community Experiments

The MaleCNS release (esp. Sept 2026) sparked a creative wave on X. Examples of projects circulating:

- Simulated MaleCNS controlling agents in **Minecraft**.
- Connectome-driven **Beat Saber** saber swinging (RL-trained).
- Fruit-fly brain “playing” **Doom** and other games.
- Live simulation processing market data to place trades on **Polymarket**.
- NFT collection launch driven by simulated walking/cursor control (flynft.online).
- NeuroMechFly-style animations typing CLI commands (e.g., Supabase meme).
- Watching college football, courtship circuit demos, driving cars, and more absurdist experiments.

These are typically topology-inspired neural networks or simplified dynamical simulations of the published wiring diagram, not literal biological tissue. They demonstrate accessibility of the open data and the power of modern simulation + RL tooling.

Search X for recent posts combining “MaleCNS”, “fruit fly connectome”, “FlyWire”, or specific demos for the latest wave.

## Related Projects & Ecosystem

- **Janelia FlyEM Project Team** — Core producers of many EM volumes and connectomes.
- **FlyWire Consortium** (Princeton + global collaborators) — Crowdsourced proofreading and annotation.
- **Cambridge Connectomics Group** / MRC LMB (Jefferis lab) — Major annotation and comparative work.
- **Google Research** — AI/ML contributions to reconstruction and scale.
- Ongoing vertebrate efforts (larval zebrafish, *Danionella*, mouse) building on fly lessons.
- Comparative resources and multi-connectome cell typing pipelines.

## Learning Resources

- FlyWire Academy — Educational materials for students.
- Official project blogs (Google Research, Janelia, HHMI, MRC LMB, Princeton Neuroscience Institute).
- Nature / Cell / Science news & views accompanying major releases.
- YouTube / project videos of cell-type galleries and example pathways (Philip Hubbard and others).
- GitHub tutorial repositories for getting started with data access and analysis.

## Contributing

Contributions are highly encouraged! Especially:

- New simulation demos or GitHub repos
- Updated links / new paper releases
- Tools, notebooks, or visualization galleries
- High-quality community experiments

A local CLI bot can help research, verify links, pull metrics, or draft PRs. Open an issue or PR following standard Awesome List conventions.

---

**License**: CC0 / Public Domain (list structure). Individual resources retain their original licenses (most connectome data is openly available under permissive terms such as CC-BY).

*Last major update: September 2026 — timed with the MaleCNS viral wave.*  
*Fly on! 🪰*