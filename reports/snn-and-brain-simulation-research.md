# Spiking Neural Networks and Brain Simulation: State of the Art and Latest Developments

*Research report compiled November 2026*

---

## Table of Contents

1. [Introduction](#introduction)
2. [Spiking Neural Networks: Fundamentals](#spiking-neural-networks-fundamentals)
3. [Key Software Frameworks](#key-software-frameworks)
4. [Neuromorphic Hardware](#neuromorphic-hardware)
5. [Latest Developments (2024–2026)](#latest-developments-20242026)
6. [Comparison: SNNs vs. Transformer LLMs](#comparison-snns-vs-transformer-llms)
7. [Open Challenges](#open-challenges)
8. [References and Further Reading](#references-and-further-reading)

---

## Introduction

Spiking Neural Networks (SNNs) represent the third generation of artificial neural network models, moving beyond rate-coded artificial neurons to models that explicitly incorporate time and discrete electrical pulses (spikes) as information carriers. This report surveys the landscape of SNN frameworks, neuromorphic hardware, and brain simulation tools, with emphasis on recent advances through 2026.

---

## Spiking Neural Networks: Fundamentals

### Core Concept
In an SNN, neurons do not continuously transmit values. Instead, they:
1. **Integrate** incoming signals over time (membrane potential accumulates)
2. **Fire** when potential crosses a threshold (emits a spike)
3. **Reset** after firing

The most common computational neuron model is the **Leaky Integrate-and-Fire (LIF)** model, which balances biological fidelity with computational tractability.

### Information Coding
SNNs encode information through:
- **Rate coding**: Frequency of spikes over time
- **Temporal coding**: Precise timing of individual spikes
- **Population coding**: Patterns across groups of neurons

### Why SNNs Matter
- **Energy efficiency**: Event-driven computation — neurons only activate when needed
- **Natural temporal processing**: Built-in handling of time-series and streaming data
- **Hardware potential**: Ideal for neuromorphic chips that operate at milliwatt power levels
- **Biological plausibility**: Closer to how actual brains operate

### Training Challenges
The all-or-nothing spike makes standard backpropagation difficult. Current approaches include:
- Surrogate gradient methods
- Spike-timing-dependent plasticity (STDP)
- Conversion of trained rate-based ANNs to SNNs
- Reinforcement learning approaches

---

## Key Software Frameworks

### Dedicated SNN Simulators

| Framework | Key Features | Best For |
|-----------|-------------|----------|
| **Brian 2** | Write differential equations directly in Python; highly flexible | Neuroscience research, custom neuron models |
| **NEURON** | Detailed biophysics (ion channels, dendrites); industry standard | Detailed neuronal biophysics |
| **NEST** | Optimized for large-scale networks (100M+ neurons) | Systems neuroscience, large networks |
| **Nengo** | Builds brain-inspired models from simplified equations | Cognitive modeling, brain-inspired computing |
| **Geppetto/OpenWorm** | Open-source visualization and simulation platform | Digital organism simulation, education |

### Deep Learning Integrated SNN Libraries

| Framework | Description |
|-----------|-------------|
| **snnTorch** | PyTorch-based SNN library with gradient-based training |
| **Norse** | Deep learning framework for SNNs (PyTorch/JAX) |
| **Lava** | Intel's open-source neuromorphic software framework for Loihi 2 |
| **Pynn** | Python API for portable SNN simulation |

### Brain Simulation Platforms

| Platform | Scale | Approach |
|----------|-------|----------|
| **Blue Brain Project** | Mouse brain (whole) | Biologically detailed digital reconstruction |
| **OpenWorm** | C. elegans (302 neurons) | Open-source complete organism simulation |
| **BrainScaleS** | 864x real-time | Hybrid neuromorphic supercomputer |

---

## Neuromorphic Hardware

### Major Chips and Systems

| System | Developer | Key Specs |
|--------|-----------|-----------|
| **Loihi 2** | Intel | Up to 10x faster than Loihi; 1.15 billion neurons in Hala Point system |
| **TrueNorth** | IBM | 1 million neurons, 256 million synapses on one chip |
| **SpiNNaker** | Univ. of Manchester | Millions of processing cores for large-scale simulation |
| **BrainScaleS** | Univ. of Heidelberg | Analog/digital hybrid; 864x real-time acceleration |
| **Neurogrid** | Stanford | 65,536 neurons across 16 chips |
| **DYNAP-SE** | ETH Zurich/INI Labs | Mixed-signal; real-time feedback learning |
| **Kapoho Point** | Intel | 8-chip Loihi 2 board; stacks for large workloads |

### Intel Hala Point (2024–2025)
The industry's first 1.15 billion neuron neuromorphic system. Achieves over 10x more neuron capacity and up to 12x higher performance than first-generation research systems. Represents the largest-scale neuromorphic deployment to date.

### Emerging Materials
Research into **memristors** and **phase-change memory** aims to create hardware that more closely emulates synaptic behavior with lower power consumption.

---

## Latest Developments (2024–2026)

### Hala Point Neuromorphic System
Intel unveiled Hala Point as the world's largest neuromorphic system with 1.15 billion neurons. It demonstrates the path toward commercially viable neuromorphic computing, with over 10x neuron capacity compared to first-generation research systems.

### Loihi 2 Processor
Intel's second-generation neuromorphic processor delivers up to 10x faster processing than its predecessor. It ships with the Lava software framework, supporting multiple AI methods and hardware for developing neuro-inspired applications.

### Memristive Systems
Significant progress has been made in developing memristor-based synapses that can:
- Perform spike-timing-dependent plasticity (STDP) learning
- Operate at low voltages approaching biological neuron thresholds
- Enable in-memory computation for ultra-low-power inference

### 3D Integration for Neuromorphic Scaling
Research groups are exploring 3D stacking and integration techniques to achieve denser neuromorphic circuits, addressing the connectivity bottleneck that has limited scaling.

### Chemical/Wetware Neuromorphic Systems
Recent research (2024) has demonstrated that chemical systems in liquid solutions can detect sound at various wavelengths, opening the door to "wetware" neuromorphic applications that blur the line between electronics and biology.

### Neuroengineering with Neuromorphic Twins
The concept of "neuromorphic twins" — digital replicas that mirror biological neural activity for research and medical applications — is gaining traction in neuroengineering.

### Organic Artificial Spiking Neurons
Researchers have developed organic artificial spiking neurons for in-situ neuromorphic sensing and biointerfacing, enabling direct interaction between neuromorphic systems and biological tissue.

---

## Comparison: SNNs vs. Transformer LLMs

| Aspect | Transformer LLM (GPT, Claude) | Spiking Neural Network |
|--------|-------------------------------|------------------------|
| **Signal type** | Continuous floating-point activations | Binary spikes (0 or 1 events) in time |
| **Computation** | Dense matrix multiplications every layer | Event-driven, sparse, threshold-triggered |
| **Training** | Backpropagation + gradient descent | Surrogate gradients, STDP, ANN→SNN conversion |
| **Scale today** | Billions–trillions of parameters | Typically thousands–millions of neurons |
| **Capabilities** | Language reasoning, code, general knowledge | Pattern recognition, temporal processing, robotics |
| **Hardware** | GPUs/TPUs (high power: hundreds of W) | Neuromorphic chips (mW range) |
| **Time handling** | Injected as sequence/position | Intrinsic (membrane dynamics, temporal coding) |
| **Maturity** | Commercially mature | Research/early commercial phase |
| **Energy per operation** | Relatively high | Potentially orders of magnitude lower |

**Bottom line:** Transformers and SNNs are complementary rather than competing. Transformers dominate tasks requiring massive scale and language understanding; SNNs show promise for edge AI, robotics, sensory processing, and ultra-low-power applications where event-driven computation matters.

---

## Open Challenges

1. **Training at scale**: No SNN training method has yet matched the scalability of backpropagation for large networks
2. **Benchmark gaps**: SNNs still lag ANNs on many standard benchmarks, though the gap is narrowing
3. **Software ecosystem**: Less mature than PyTorch/TensorFlow ecosystems
4. **Interpretability**: Understanding why and how SNNs make decisions remains difficult
5. **Biological vs. computational trade-off**: More biologically accurate models are often less computationally efficient
6. **Hardware adoption**: Neuromorphic chips are not yet mainstream or widely supported by software

---

## References and Further Reading

### Academic Papers and Perspectives
1. **Ham, D., Park, H., Hwang, S., & Kim, K. (2021).** "Neuromorphic electronics based on copying and pasting the brain." *Nature Electronics*, 4, 635–644.
   - URL: https://www.nature.com/articles/s41928-021-00646-1
   - Vision for returning neuromorphic engineering to rigorous brain mimicry using copy-and-paste of functional synaptic connectivity maps.

2. **Davies, M., et al. (2018).** "Loihi: A Neuromorphic Manycore Processor with On-Chip Learning." *IEEE Micro*, 38(1), 82–99.
   - URL: https://doi.org/10.1109/MM.2018.112130359
   - Original publication describing Intel's Loihi neuromorphic processor.

3. **Merolla, P., et al. (2014).** "A million spiking-neuron integrated circuit with a scalable communication network and interface." *Science*, 345, 668–673.
   - URL: https://doi.org/10.1126/science.1254642
   - IBM's TrueNorth chip publication.

4. **Boahen, K. (2014).** "Neurogrid: A Mixed-Analog-Digital Multichip System for Large-Scale Neural Simulations." *Proceedings of the IEEE*, 102(5), 699–716.
   - URL: https://doi.org/10.1109/JPROC.2014.2313565
   - Stanford's Neurogrid system.

5. **Moradi, S., et al. (2018).** "A scalable multicore architecture with heterogeneous memory structures for dynamic neuromorphic asynchronous processors (DYNAPs)." *IEEE Transactions on Biomedical Circuits and Systems*, 12(1), 106–122.
   - URL: https://doi.org/10.1109/TBCAS.2017.2759700
   - ETH Zurich's DYNAP-SE architecture.

### Software and Tool Documentation
6. **Brian 2 documentation** — https://briansimulator.org/
   - Comprehensive documentation for Brian 2 SNN simulator.

7. **NEURON documentation** — https://neuron.yale.edu/
   - Gold-standard tool for detailed neuronal biophysics simulation.

8. **NEST documentation** — https://nest-simulator.org/
   - Simulator optimized for large-scale neural network modeling.

9. **snnTorch documentation** — https://snntorch.readthedocs.io/en/latest/
   - PyTorch-based spiking neural network library.

10. **Norse documentation** — https://norse.readthedocs.io/
    - Deep learning framework for SNNs in PyTorch/JAX.

### Neuromorphic Hardware and Projects
11. **Intel Neuromorphic Computing** — https://www.intel.com/content/www/us/en/research/neuromorphic-computing.html
    - Information about Loihi, Hala Point, and Intel's neuromorphic research.

12. **Blue Brain Project** — https://bluebrain.epfl.ch/
    - EPFL's project to create biologically detailed digital reconstructions of the mouse brain.

13. **OpenWorm** — https://openworm.org/
    - Open-source project to create the first digital life form (C. elegans).

14. **BrainScaleS** — https://brainscales.kip.uni-heidelberg.de/
    - Hybrid neuromorphic supercomputer at University of Heidelberg.

### Educational Resources
15. **Wikipedia: Spiking neural network** — https://en.wikipedia.org/wiki/Spiking_neural_network
    - Overview of SNN fundamentals, history, and applications.

16. **Wikipedia: Neuromorphic computing** — https://en.wikipedia.org/wiki/Neuromorphic_computing
    - History and overview of neuromorphic engineering and computing.

---

*Report compiled by AI research agent. Sources accessed and verified November 2026.*
