# Thesis abstract
Quantum generative models leverage the probabilistic structure of quantum mechanics to learn and reproduce complex data distributions beyond classical capabilities. Among these, Born machines encode probabilities via quantum amplitudes, offering efficient sampling and expressive power. However, their scalability is hindered by issues such as barren plateaus. In this thesis, we investigate Tensor Network Born Machines (TNBMs), which integrate tensor networks into the Born machine framework to overcome training obstacles while retaining expressive power. We examine their theoretical underpinnings and practical implementation for learning quantum data distributions. Additionally, we explore the use of positive operator-valued measures (POVMs) for informationally complete measurements, inspired by classical shadow tomography, as a means to enhance the learning capabilities of TNBMs by capturing higher-order correlations and enabling more efficient training.



# Introduction
Generative models have become indispensable tools for learning complex data distributions and generating new samples that resemble the original dataset. In the quantum domain, these models take on heightened significance as they leverage the inherently probabilistic nature of quantum systems to capture and reproduce "quantum data." By exploiting quantum mechanics, these models can encode probability distributions that are inaccessible to classical approaches, offering efficient sampling mechanisms and paving the way for diverse applications in physics [4-9,15].

Two prominent quantum generative models stand out for their physical foundations: Boltzmann machines and Born machines. Boltzmann machines utilize the Boltzmann distribution from statistical mechanics to represent joint probability distributions [1], while Born machines rely on Born's rule, encoding probabilities as squared amplitudes of wavefunctions [2–5].

Despite their promise, quantum generative models face significant challenges, particularly in scalability. Issues such as barren plateaus and loss concentration —regions where gradients vanish exponentially— hinder effective training of large-scale systems[11]. To address these limitations, Tensor Network Born Machines[3,12-14] (TNBMs) have emerged as a robust alternative. By incorporating tensor networks into the Born machine framework, TNBMs mitigate barren plateau problems while maintaining the expressivity advantages of quantum-inspired models [10]. This approach represents a critical step forward in overcoming trainability barriers and enhancing the performance of quantum generative models.

In this my master thesis, we explore the theoretical foundations and practical implementations of Tensor Network Born Machines, demonstrating their ability to model complex quantum data distributions while addressing key scalability challenges.

Traditional Born machines often rely on projective measurements in the computational basis, which restrict the information extracted during training. Inspired by classical shadow tomography techniques and previous work [15-17], we adopt positive operator-valued measures (POVMs) to perform informationally complete measurements[3,18,19]. By sampling from a diverse set of observables, POVMs enable efficient reconstruction of quantum states and their underlying distributions. This approach captures higher-order correlations in the data, overcoming the limitations of fixed-basis measurements and ensuring robust learning of complex probability distributions.[13,15,20]

# Conclusions and future directions
While TNBMs excel at modeling discrete distributions, their application to continuous data has been hindered by the infinite-dimensional local spaces required for continuous variables. We resolve this by introducing vector-valued feature maps that project continuous domains into finite-dimensional feature spaces[15].

# Bibliography
[1] G. E. Hinton and T. J. Sejnowski, Learning and relearning in Boltzmann machines, in Parallel Distributed Processing: Explorations in the Microstructure of Cognition (MIT Press, Cambridge, MA, 1986), Vol. 1, pp. 282–317.

[2] Differentiable Learning of Quantum Circuit Born Machine
Jin-Guo Liu, Lei Wang

[3] Z.-Y. Han, J. Wang, H. Fan, L. Wang, and P. Zhang, Unsu-
pervised Generative Modeling Using Matrix Product States,
Phys. Rev. X 8, 031012 (2018).

[4] Perdomo-Ortiz, A., Benedetti, M., Realpe-Gómez, J. & Biswas, R. Opportunities and challenges for quantum-assisted machine learning in near-term quantum computers. Quantum Sci. Technol. 3, 030502 (2018).

[5] Coyle, B., Mills, D., Danos, V. & Kashefi, E. The born supremacy: quantum advantage and training of an ising born machine. npj Quantum Inf. 6, 60 (2020).

[6] Sweke, R., Seifert, J.-P., Hangleiter, D. & Eisert, J. On the quantum versus classical learnability of discrete distributions. Quantum 5, 417 (2021).

[7] Gao, X., Anschuetz, E. R., Wang, S.-T., Cirac, J. I. & Lukin, M. D. Enhancing generative models via quantum correlations. Phys. Rev. X 12, 021037 (2022).

[8] Kiss, O., Grossi, M., Kajomovitz, E. & Vallecorsa, S. Conditional born machine for monte carlo event generation. Phys. Rev. A 106, 022612 (2022).

[9] Delgado, A. & Hamilton, K. E. Unsupervised quantum circuit learning in high energy physics. Phys. Rev. D 106, 096006 (2022).

[10] Barren plateaus in quantum tensor network optimization Enrique Cervero Martín Kirill Plekhanov, and Michael Lubasch
2023-04-13, volume 7, page 974 arXiv:2209.00292v3

[11] Rudolph, M.S., Lerch, S., Thanasilp, S. et al. Trainability barriers and opportunities in quantum generative modeling. npj Quantum Inf 10, 116 (2024). https://doi.org/10.1038/s41534-024-00902-0

[12] Tree tensor networks for generative modeling Song Cheng, Lei Wang, Tao Xiang, and Pan Zhang

[13] Alex Meiburg, undefined., et al. "Generative learning of continuous data by tensor networks," in SciPost Phys., vol. 18, pp. 096, 2025.

[14] Regularized second-order optimization of tensor-network Born machines
Matan Ben-Dov, Jing Chen

[15] Rudolph, M., et al. "Generation of High-Resolution Handwritten Digits with an Ion-Trap Quantum Computer," in Phys. Rev. X, vol. 12, pp. 031010, 2022.

[16] Levy, R., Luo, D., & Clark, B. (2024). Classical shadows for quantum process tomography on near-term quantum computers. Phys. Rev. Res., 6, 013029.

[17] Jerbi, S., Gyurik, C., Marshall, S.C. et al. Shadows of quantum machine learning. Nat Commun 15, 5676 (2024). https://doi.org/10.1038/s41467-024-49877-8

[18] Stefano Mangini, & Daniel Cavalcanti. (2024). Low-variance observable estimation with informationally-complete measurements and tensor networks.

[19] García-Perez, G., Rossi, M., Sokolov, B., Tacchino, F., Barkoutsos, P., Mazzola, G., Tavernelli, I., & Maniscalco, S. (2021). Learning to Measure: Adaptive Informationally Complete Generalized Measurements for Quantum Algorithms. PRX Quantum, 2, 040342.

[20] Ema Puljak, Sergio Sanchez-Ramirez, Sergi Masot-Llima, Jofre Vallès-Muns, Artur Garcia-Saez, & Maurizio Pierini. (2025). tn4ml: Tensor Network Training and Customization for Machine Learning. 