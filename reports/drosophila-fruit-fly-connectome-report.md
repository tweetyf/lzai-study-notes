# The Drosophila Connectome Project: Complete Map of the Fruit Fly Brain and Central Nervous System

*A comprehensive report on the largest brain map to date*
*Compiled November 2026*

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [Project Overview](#project-overview)
3. [Timeline and Milestones](#timeline-and-milestones)
4. [Technical Approach](#technical-approach)
5. [The Complete Male CNS Connectome (2026)](#the-complete-male-cns-connectome-2026)
6. [Key Scientific Discoveries](#key-scientific-discoveries)
7. [Comparison: Male vs. Female Fruit Fly Brains](#comparison-male-vs-female-fruit-fly-brains)
8. [Tools and Data Access](#tools-and-data-access)
9. [Impact and Legacy](#impact-and-legacy)
10. [Future Directions](#future-directions)
11. [References](#references)

---

## Executive Summary

In September 2026, an international consortium led by HHMI's Janelia Research Campus, the MRC Laboratory of Molecular Biology at Cambridge, and Google Research published the **complete connectome of the male Drosophila (fruit fly) central nervous system**. This landmark achievement, published in *Cell*, maps all **166,700 neurons** and **125 million synaptic connections** in the fly's brain, optic lobes, and ventral nerve cord.

This project represents:
- **The largest brain map ever created** by number of neurons
- A **20-year research journey** from initial concept to completion
- The first comprehensive comparison of male and female fruit fly brains at synapse resolution
- A foundational resource for understanding how neural circuits generate complex behavior

The completion of the male CNS connectome complements the previously published female brain map and the female CNS map, enabling unprecedented comparative studies of sexual dimorphism in the nervous system.

---

## Project Overview

### What is Connectomics?
Connectomics is the study of the complete wiring diagram (connectome) of a nervous system — mapping every neuron and every synaptic connection. The field aims to understand how the physical structure of neural circuits relates to brain function and behavior.

### Why the Fruit Fly?
*Drosophila melanogaster* (the fruit fly) was chosen as a model organism for connectomics because:
- It has a relatively small nervous system (~150,000 neurons) compared to vertebrates
- It exhibits complex behaviors (mating, navigation, aggression, learning)
- It has well-established genetic tools
- Many findings translate to understanding higher organisms

### Project Goals
1. Create a complete, synapse-resolution wiring diagram of the adult fruit fly brain and CNS
2. Develop the imaging and computational techniques necessary for such large-scale mapping
3. Enable the scientific community to study how neural circuits generate behavior
4. Provide a foundation for comparative connectomics across sexes and species

---

## Timeline and Milestones

| Year | Milestone |
|------|-----------|
| **2006** | Project conception begins at Janelia Research Campus |
| **2008** | Janelia officially commits to the fruit fly connectome project |
| **2009-2015** | Development and optimization of imaging and computational techniques |
| **2015** | First small connectomes mapped (medulla, optic lobe regions) |
| **2019** | Google Research releases fully-automated reconstruction of female fly brain |
| **2020** | **Hemibrain connectome** published (25,000 neurons, half a female brain) — the biggest and most detailed connectome at the time |
| **2022** | Female optic lobe connectome completed |
| **2024** | Complete female brain connectome published |
| **2025** | Initial female CNS connectome released |
| **October 2025** | Preprint of male CNS connectome on bioRxiv |
| **June 2026** | MaleCNS v1.0 released to public |
| **September 3, 2026** | **Official publication in Cell** — complete male CNS connectome with 166,700 neurons and 125 million synapses |

---

## Technical Approach

### Imaging: Enhanced Focused Ion Beam Scanning Electron Microscopy (eFIB-SEM)
The nervous system was sliced into incredibly thin sections (30-40 nanometers thick) and imaged using high-resolution focused ion beam scanning electron microscopy. This technique provides the resolution needed to identify individual neurons and their synapses.

### Image Processing Pipeline
1. **Data Acquisition**: Millions of 2D electron microscopy images are collected
2. **Volume Reconstruction**: Images are stacked to create a 3D volume
3. **Segmentation**: AI algorithms identify and trace individual neurons from the 3D volume
4. **Synapse Detection**: Machine learning models identify and classify synapses
5. **Proofreading**: Human experts at Janelia and Cambridge verify and correct the automated reconstructions
6. **Annotation**: Neurons are classified into cell types and labeled

### AI and Machine Learning
Google Research played a crucial role in developing the computational tools:
- **Flood-filling networks**: Convolutional neural networks that identify all pixels belonging to the same neuron
- **PATHFINDER**: State-of-the-art reconstruction system using synthetic training data
- **Neuroglancer**: Open-source visualization tool for huge multidimensional datasets

### Scale of Human Effort
The project required the equivalent of **44 years of human labor** for reconstruction, proofreading, and annotation by hundreds of researchers over two decades.

---

## The Complete Male CNS Connectome (2026)

### Key Statistics
| Metric | Value |
|--------|-------|
| Neurons | 166,700 |
| Synapses | 125 million |
| Cell Types | 11,710 |
| Regions Mapped | Central brain, both optic lobes, ventral nerve cord |
| Dataset Size | Petabytes of imaging data |

### What's Included
The male CNS connectome encompasses:
- **Central brain**: Higher-order processing regions
- **Optic lobes**: Visual processing centers (analogous to mammalian retina)
- **Ventral nerve cord**: Analogous to the spinal cord; controls body movements
- **Neck connective**: First connectome with an intact neck, linking brain and nerve cord

This is the first complete map that connects the entire nervous system from sensory input to motor output.

---

## Key Scientific Discoveries

### Sexual Dimorphism in the Fly Brain
Comparing the male and female connectomes revealed fascinating insights into how sex differences are encoded in neural circuitry:

1. **Small but Impactful**: Only ~4.8% of male brain neurons (and <3% in females) are sex-specific or sexually dimorphic. However, these neurons make many connections, affecting ~12% of the male brain's wiring.

2. **Concentration in Higher Brain Centers**: Sex-specific and dimorphic neurons are concentrated in higher-order brain regions associated with decision-making and behavioral control, not in sensory or motor periphery.

3. **Circuit Switches**: Circuit "switches" reroute the same sensory information into different behavioral pathways depending on sex. This explains how identical stimuli can trigger different responses in males and females.

4. **Male-Specific Network**: About 100 male-specific interneuron cell types form a highly intertwined network in the central brain that coordinates most male-specific behaviors.

5. **Genetic Basis**: Many dimorphic neurons express the sex-determination genes *fruitless* and *doublesex*.

### Visual Processing
Tracing signals from the eye through the complete connectome revealed:
- Visual processing extends deep into the brain, engaging more than half of all neuron types
- Functional predictions for thousands of physiologically uncharacterized neuron types
- Understanding of which visual channels drive each neuron, how strongly, and from where in the visual field

### Taste System
The complete map of the fly taste system shows:
- How taste neurons carrying attractive vs. repulsive signals connect to different circuits
- Connections to circuits controlling feeding, locomotion, hormone release, and courtship
- How internal states can shape taste-driven decisions independent of external stimuli

### Behavioral Circuits
The connectome enables tracing complete neural circuits from sensory perception to behavior, including:
- Navigation to goals
- Mating behaviors
- Aggression
- Feeding decisions

---

## Comparison: Male vs. Female Fruit Fly Brains

| Feature | Male | Female |
|---------|------|--------|
| Total neurons | 166,700 | ~150,000 |
| Sex-specific neurons | 262 types | Fewer types |
| Sexually dimorphic neurons | 114 types | Different patterns |
| % of brain affected by dimorphism | ~12% | ~4% |
| Published | September 2026 | Brain: 2024; CNS: in progress |

### What This Means
- Sensory and motor circuits are largely shared (isomorphic) between sexes
- Behavioral differences arise from higher-level circuit switches, not fundamentally different sensory processing
- A small fraction of neurons can exert brain-wide influence through their connectivity patterns

---

## Tools and Data Access

The connectome data and tools are freely available to the scientific community:

### Exploration Tools
- **MaleCNS Connectome Site** (janelia-flyem.github.io/male-cns/): Compare connectivity of dimorphic cells across male and female connectomes
- **NeuPrint** (neuprint.janelia.org): Explore the connectome with connectivity queries
- **Cell Type Explorer**: Browse cell types and type-to-type connectivity
- **Clio**: Annotation-focused interface for finding neurons
- **Neuroglancer**: Open-source tool for visualizing multidimensional datasets

### Programmatic Access
- **neuprint-python**: Python API for programmatic access
- **malecns R package**: From the natverse collection

### Data Downloads
- Image volumes
- Annotations
- Connectivity tables
- Neuron meshes and skeletons

All data is licensed under **CC-BY** for open reuse.

---

## Impact and Legacy

### Advancing Connectomics
The fruit fly project:
- Proved that whole-brain connectomics at synapse resolution is feasible
- Developed techniques that reduced the time and cost of connectome generation by more than 1,000-fold
- Paved the way for connectome projects of more complex organisms

### Transforming Neuroscience
- Changed the attitude of neuroscientists about what's possible with connectomics
- Provided a comprehensive reference for understanding neural circuits
- Enabled new approaches to studying behavior at the circuit level

### Technological Innovations
- Pioneered new imaging technologies (eFIB-SEM)
- Advanced AI and machine learning for image analysis
- Created open-source tools (Neuroglancer) now used across many fields

### Educational Impact
- Trained hundreds of scientists in connectomics techniques
- Established best practices for large-scale biological data projects
- Demonstrated the power of international collaboration

---

## Future Directions

### From Invertebrates to Vertebrates
Janelia is now applying lessons from the fruit fly project to vertebrate models:

1. **Larval Zebrafish**: A whole-brain connectome is being completed that includes neuronal activity data
2. **Adult Danionella**: A transparent fish species is being mapped for the first vertebrate adult connectome

### Molecular Annotation
The AI@HHMI project led by Gerry Rubin aims to create molecularly annotated connectomes that provide information about the signals passed between neurons — adding a functional dimension to the structural maps.

### Predictive Models
Misha Ahrens' project uses the larval zebrafish connectome with whole-brain activity recordings to create predictive models of brain function.

### Ultimate Goal
To provide the first mechanistic account of how a vertebrate brain generates complex behavior — information that could help unravel brain function and potentially reveal how diseases like Alzheimer's and depression arise.

---

## References

1. **Berg, S., et al. (2026).** "Sexual dimorphism in the complete connectome of the Drosophila male central nervous system." *Cell*. DOI: 10.1016/j.cell.2026.08.015

2. **Janelia Research Campus.** "Researchers Reveal Connectome of the Male Fruit Fly Central Nervous System." https://www.janelia.org/news/researchers-reveal-connectome-of-the-male-fruit-fly-central-nervous-system

3. **HHMI.** "Scientists Complete Full Map of the Fruit Fly Central Nervous System." https://www.hhmi.org/news/scientists-complete-full-map-fruit-fly-brain-connectome

4. **Google Research Blog.** "A connectomics milestone: Mapping the complete male fruit fly brain." September 3, 2026. https://research.google/blog/a-connectomics-milestone-mapping-the-complete-male-fruit-fly-brain/

5. **MRC LMB.** "First complete connectome of male fly central nervous system allows for unprecedented male-female brain comparison." September 3, 2026. https://mrclmb.ac.uk/news-events/articles/first-complete-connectome-of-male-fly-central-nervous-system-allows-for-unprecedented-male-female-brain-comparison/

6. **Science/AAAS.** "New 'connectome' shows all 124 million contact points in the fruit fly's nervous system." September 3, 2026.

7. **Ars Technica.** "Second complete map of a fruit fly brain completed." September 4, 2026. https://arstechnica.com/science/2026/09/brain-of-a-male-fly-completely-mapped-joins-earlier-map-of-a-female-brain/

8. **Male CNS Connectome Project Page.** https://www.janelia.org/project-team/flyem/male-cns-connectome

9. **Cell Consortium Collection.** "Male Fly Connectome." https://www.cell.com/consortium/male-fly-connectome

---

*This report was compiled from publicly available sources in November 2026. The Drosophila connectome project represents one of the most significant achievements in modern neuroscience and a testament to the power of long-term, interdisciplinary scientific collaboration.*
