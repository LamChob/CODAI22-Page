# News
 - September 28<sup>th</sup> 2022: Program added
 - August 18<sup>th</sup> 2022: Deadline extension
 - June 8<sup>th</sup> 2022: [Call for papers for CODAI'22 workshop](assets/documents/codai22_cfp.pdf) published
 - May 12<sup>th</sup> 2022: CODAI has been accepted at **Embedded Systems Week 2022**



# Overview

**CODAI'22** is an  [Embedded Systems Week](https://esweek.org/ ) workshop to coalesce the emerging energy in the AI compiler communities and AI accelerator communities focusing on Edge AI in both academic and industrial research. These realms of research have the opportunity to deliver a pervasive and seamless end-to-end tooling that connects hardware and software development methodologies. This workshop mainly focuses on:
 - Discussing new impulses for deployment of Neural Networks on low-end embedded systems
 - Cooperative development of (open source) toolchains/frameworks for neural network deployment + cooperation between industry and academia

Therefore, it **complements the established conferences** CASES and CODES+ISSS which have a wider and more academic research-spectrum.
We also welcome work-in-progress papers of ongoing research projects and case studies from industrial applications.

Topics for workshop submissions include, but are not limited to:

 - Optimization techniques of neural networks on embedded edge systems: **compression, pruning, quantization techniques,
  hardware/compiler-aware neural architecture search**, etc.
 - Performance estimation of neural networks on embedded systems: **virtual prototyping, surrogate modeling, profiling** etc.
 - Compilers for Edge AI: **partitioning, mapping, retargeting, intermediate representations,
   for heterogeneous systems and architectures, µC, DSP** etc.
 - Code-generation and compiler-backends for AI accelerators - especially for **RISC-V**
  and **beyond-von-Neumann AI accelerators** is appreciated
 - Applications: processing of **embedded vision, sensor signal processing, novel brain-inspired algorithms for Edge AI** etc.



# Program
**CODAI'22** will take place on *October 13<sup>th</sup> 2022* as virtual workshop.


## Schedule
| PDT (LA) | EDT (NY) | CEST (Berlin) | CST (Shanghai) | Title                                                                                                     | Speaker                                                                                | Affiliation                                                                                          |Slides
|---------|----------|---------------|----------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------|
| 7:00    | 10:00    | 16:00         | 22:00          | Introduction                                                                                              |                                                                                        |                                                                                                      |
| 7:15    | 10:15    | 16:15         | 22:15          | Industrial Keynote                                                                                        | Kailash Gopalakrishnan                                                                 | EnCharge AI                                                                                          |
| 8:05    | 11:05    | 17:05         | 23:05          | Performance models and energy-optimal mapping of DNNs on many-core hardware with dynamic power management | Bernhard Vogginger, Florian Kelber, Johannes Partzsch and Christian Mayr               | TU Dresden                                                                                           |
| 8:30    | 11:30    | 17:30         | 23:30          | HyT-NAS: Hybrid Transformers Neural Architecture Search for Edge Devices                                  | Lotfi Abdelkrim Mecharbat, Hadjer Benmeziane, Ouarnoughi Hamza and Smail Niar          | Ecole Nationale Supérieure d'Informatique, Hauts-de-France, Université Polytechnique Hauts-de-France |
| 8:55    | 11:55    | 17:55         | 23:55          | Whole-model optimization with Apache TVM                                                                  | Andrew Reusch                                                                          | OctoML                                                                                               |
| 9:20    | 12:20    | 18:20         | 0:20           | MLonMCU: TinyML Benchmarking with Fast Retargeting                                                        | Philipp van Kempen, Rafael Stahl, Daniel Müller-Gritschneder and Ulf Schlichtmann      | Technical University of Munich                                                                       | [PDF](slides/codai22_mlonmcu_slides.pdf)
| 9:45    | 12:45    | 18:45         | 0:45           | Break                                                                                                     |                                                                                        |                                                                                                      |
| 10:00   | 13:00    | 19:00         | 1:00           | Academic Keynote                                                                                          | Tianqi Chen                                                                            | Carnegie Mellon University                                                                           |
| 10:50   | 13:50    | 19:50         | 1:50           | Embedded AI Challenges in Perception Systems                                                              | Miguel Aguilar                                                                         | Aptiv                                                                                                |
| 11:15   | 14:15    | 20:15         | 2:15           | Integration of a systolic array based hardware accelerator into a DNN operator auto-tuning framework      | Federico Nicolás Peccia and Oliver Bringmann                                           | FZI Research Center for Information Technology, University of Tübingen                               |
| 11:40   | 14:40    | 20:40         | 2:40           | Deploying Machine Learning Models to Ahead-of-Time Runtime on Edge Using MicroTVM                         | Chen Liu, Liyuan Guo, Xinyue Shi, Matthias Jobst, Johannes Partzsch and Christian Mayr | Chair of Highly-Parallel VLSI-Systems and Neuromorphic Circuits, TU Dresden                          |
| 12:05   | 15:05    | 21:05         | 3:05           | Conclusion                                                                                                |                                                                                        |                                                                                                      |

## Abstracts
| Title                                                                                                     | Speaker                                                                                | Abstract                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Performance models and energy-optimal mapping of DNNs on many-core hardware with dynamic power management | Bernhard Vogginger, Florian Kelber, Johannes Partzsch and Christian Mayr | Processing of deep neural networks (DNNs) at the edge may be limited by power or energy constraints of the used embedded hardware system. It is therefore desirable for the compiler to create efficient executables for given DNN models meeting the specific constraints. Here, we consider a low-power many-core hardware with 152 processing elements, each containing an ARM M4F processor, 128 KB SRAM and a custom accelerator for DNN inference. Dynamic power management allows each core to switch between a high-speed and a low-power mode within tens of nanoseconds. For an energy-optimal parallelization of DNNs on the hardware, we first develop analytical performance models to predict the time and energy for executing a DNN layer with the custom accelerator. The models are fitted and validated using measurements on a prototype chip. In a second step we develop concepts for the energy-optimal parallelization of DNNs under latency constraints and evaluate them deploying the performance models: By dynamically switching between the operating modes more than 10% of energy can be saved compared to the case running at high-speed mode only. The presented methodology and concepts are easily transferable to other many-core edge processors.|
| HyT-NAS: Hybrid Transformers Neural Architecture Search for Edge Devices                                  | Lotfi Abdelkrim Mecharbat, Hadjer Benmeziane, Ouarnoughi Hamza and Smail Niar          | Vision Transformers have enabled recent attention-based Deep Learning architectures to achieve remarkable results in Computer Vision (CV) tasks. However, due to the extensive computational resources required, these architectures are rarely implemented on resource-constrained platforms. Current research investigates hybrid handcrafted convolution-based and attention-based models for CV tasks such as image classification and object detection. In this paper, we propose HyT-NAS, an efficient Hardware-aware Neural Architecture Search including hybrid architectures targeting vision tasks on tiny devices. HyT-NAS improves state-of-the-art HW-NAS by enriching the search space and enhancing the search strategy as well as the performance predictors. Our experiments show that HyT-NAS achieves a similar hypervolume with less than 5x training evaluations. Our resulting architecture outperforms MLPerf MobileNetV1 by 6.3% accuracy improvement with 3.5x less number of parameters on Visual Wake Words. |
| Whole-model optimization with Apache TVM                                                                  | Andrew Reusch (OctoML) | Optimized deep learning kernels are crucial for achieving good performance in deployed ML models. Increasingly, developers are turning to deployment tools to assemble these optimized kernels into full models. However, per-kernel optimizations have limited impact on a full model’s throughput, especially when heterogenous compute platforms are in use or when the underlying hardware is designed to execute operators concurrently. <br /><br /> In this talk, I’ll describe how Relax, a new model-level language in Apache TVM, enables hardware vendors to easily apply common hardware optimization techniques such as striping and global memory planning across the full program. With Relax, these techniques can be easily tailored towards both individual accelerators and heterogeneous compute environments. I’ll lastly discuss our future plans to integrate Relax with Apache TVM’s Ahead-of-Time compilation flow, making it available in a low-overhead runtime targeted to bare-metal environments. |
| MLonMCU: TinyML Benchmarking with Fast Retargeting                                                        | Philipp van Kempen, Rafael Stahl, Daniel Müller-Gritschneder and Ulf Schlichtmann      | While there exist many ways to deploy machine learning models on microcontrollers, it is non-trivial to choose the optimal combination of frameworks and targets for a given application. Thus, automating the end-to-end benchmarking flow is of high relevance nowadays. A tool called MLonMCU is proposed in this paper and demonstrated by benchmarking the state-of-the-art TinyML frameworks TFLite for Microcontrollers and TVM effortlessly with a large number of configurations in a low amount of time. |
| Embedded AI Challenges in Perception Systems                                                              | Miguel Aguilar (Aptiv)                                                                        | Recent advancements in embedded computing and especially in AI accelerators have enabled the implementation of complex AI algorithms with high computational requirements. However, the deployment of these algorithms still presents several technical challenges, some of which are general to embedded systems (e.g., memory bandwidth and parallelization), while others are specific to AI (e.g., supported layers and quantization). <br /><br /> Deploying AI models on embedded systems is an emerging and fast-changing field. In terms of perception systems, vision has been the pioneer area for embedded AI deployment. However, perception systems based on other sensor types such as Radar, Lidar and Ultrasonic are following. These sensors pose new significant challenges for embedded AI, not only due to the nature of their data, but also due to the nature of their algorithms. <br /><br /> In this talk, general embedded AI challenges from a perspective of perception systems are discussed. The presentation focuses on difficulties faced at different stages of the embedded AI implementation flow, starting from freshly trained AI models to its efficient and accurate execution on embedded systems in a cost-effective way. |
| Integration of a systolic array based hardware accelerator into a DNN operator auto-tuning framework      | Federico Nicolás Peccia and Oliver Bringmann                                           | The deployment of neural networks on heterogeneous SoCs coupled with custom accelerators is a challenging task because of the lack of end-to-end software tools provided for these systems. Moreover, the already available low-level schedules and mapping strategies provided by the accelerator developers for typical tensor operations are not necessarily the best possible ones for each particular use case. This is why frameworks which automatically test the performance of the generated code on a specific hardware configuration are of special interest. In this work, the integration between the code generation framework TVM and the systolic array-based accelerator Gemmini is presented. A generic schedule to offload the general matrix multiply tensor operation onto Gemmini is detailed, and its suitability is tested by executing the AutoTVM tuning process on it. Our generated code achieves a peak throughput of 46 giga-operations per second under a 100 MHz clock on a Xilinx ZCU102 FPGA, outperforming previous work. Furthermore, the code generated by this integration was able to surpass the default hand-tuned schedules provided by the Gemmini developers in real-world workloads. |
| Deploying Machine Learning Models to Ahead-of-Time Runtime on Edge Using MicroTVM                         | Chen Liu, Liyuan Guo, Xinyue Shi, Matthias Jobst, Johannes Partzsch and Christian Mayr | In the past few years, more and more AI applications have been applied to edge devices. However, models trained by data scientists with machine learning frameworks, such as PyTorch or TensorFlow, can not be seamlessly executed on edge. In this paper, we develop an end-to-end code generator parsing a pre-trained model to C source libraries for the backend using MicroTVM, a machine learning compiler framework extension addressing inference on bare metal devices. An analysis shows that specific compute-intensive operators can be easily offloaded to the dedicated accelerator with a Universal Modular Accelerator interface, while others are processed in the CPU cores. By using the automatically generated ahead-of-time C runtime, we conduct a hand gesture recognition experiment on an ARM Cortex M4F core. |

# Important Dates
 - **Abstract submission deadline**: August 25<sup>th</sup> 2022 AOE
 - **Paper submission deadline**: September 8<sup>th</sup> 2022 AOE  <s>August 18<sup>th</sup> 2022 AOE </s>
 - **Acceptance notification**: September 26<sup>th</sup>, 2022 <s>September 22<sup>nd</sup>, 2022 </s> <s>September 8<sup>th</sup>, 2022</s>
 - **Camera-ready paper**: October 7<sup>th</sup>, 2022 <s>September 30<sup>th</sup>, 2022</s>
 - **Workshop date**: October 13<sup>th</sup> 2022

# Call For Papers
[Call for papers for CODAI'22 workshop](assets/documents/codai22_cfp.pdf)

## Paper Submission
[Paper submission](https://easychair.org/conferences/?conf=codai22)

## Registration

[ESWEEK Registration](https://esweek.org/registration/) $15.75 / $20.00

 If you have registered the main conference, you can attend the workshop for free.

## Author Instructions

- Submit camera-ready via Easychair by October 7<sup>th</sup>, 2022
  - Use [IEEE Template](https://www.ieee.org/conferences/publishing/templates.html)
  - Paper must not exceed a length of 5 pages incl. references
- Submit slides as PPT or PDF by October 12<sup>th</sup> 2022
  - via Github pull request [here](https://github.com/LamChob/CODAI22)
  - add link to index.md

# Organization
### Organization Committee
* Michael J. Klaiber - EnCharge AI
* Sebastian Vogel - NXP Semiconductors, The Netherlands

### Program Committee
* Deming Chen - University of Illinois Urbana Champaign, USA
* Andreas Bytyn - Bosch Automotive Electronics, Germany
* Andrew Reusch - OctoML, USA
* Henk Corporaal - Eindhoven University of Technology, The Netherlands
* Robert Nabholz - RB XC, Germany
* Floran de Putter - Eindhoven University of Technology, The Netherlands
* Oliver Bringmann - University of Tübingen, Germany
* Paul Palomero Bernardo - University of Tübingen, Germany
* Falk Rehm - Bosch Research, Germany
* Dennis Rieber - Bosch Research, Germany
* Christoph Schorn - Bosch Research, Germany
* Ingo Feldner - Bosch Research, Germany
* Hussam Amrouch - University of Stuttgart, Germany
* Dayane Reis, University of South Florida, USA

### Contact

For questions contact:

Dr. Michael J. Klaiber, EnCharge AI

E-Mail: codai2022 (a) michael-klaiber.de


Logo by <a href="https://www.flaticon.com/authors/parzival-1997" title="Logo">Parzival’ 1997</a>
