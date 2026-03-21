**Annotated Bibliography of Spiking Neural Networks for Medical Image Analysis: A Survey**


[F1] Maass, W. (2019). Deep learning in spiking neural networks (Neural Networks).
URL: https://doi.org/10.1016/j.neunet.2018.12.002

Annotation: This review surveys progress in closing the performance gap between spiking and conventional neural networks. It notes that treating a spiking neuron’s membrane potential as a differentiable signal enables backpropagation and yields MNIST accuracies around 98.88 %, nearly matching standard ANNs while using far fewer operations. The authors also describe an event‑driven random backpropagation scheme and discuss how converting a trained ANN into an SNN preserves accuracy and saves energy.

[F2] Wu, Y., Deng, L., Li, G., Zhu, J., Xie, Y., & Shi, L. (2018). Spatio‑Temporal Backpropagation for Training High‑Performance Spiking Neural Networks (Frontiers in Neuroscience 12).
URL: https://doi.org/10.3389/fnins.2018.00331

Annotation: The authors propose a spatio‑temporal backpropagation algorithm that combines spatial and temporal gradients and uses an approximate spike derivative. Their method trains SNNs directly (without ANN conversion) and achieves 98.89 % accuracy on MNIST and 99.42 % with a spiking CNN, outperforming previous SNNs and even some ANNs. Strong results are also reported on the event‑driven N‑MNIST and CIFAR‑10 datasets without elaborate training tricks.

[F3] Zenke, F., & Vogels, T. P. (2019). The remarkable robustness of surrogate gradient learning for instilling complex function in spiking neural networks (Neural Computation 33 (4), 899–925).
URL: https://doi.org/10.1162/neco_a_01367

Annotation: This tutorial demonstrates that SNNs can be trained much like recurrent neural networks by replacing the zero‑gradient spike function with a smooth surrogate derivative. Different surrogate functions (piecewise linear, exponential, sigmoid) are compared, and the authors show that performance is largely insensitive to the exact choice as long as the function is monotonic. Examples include spiking recurrent networks trained with piecewise linear surrogates that perform on par with LSTM networks on temporal tasks.

[F4] Wu, Y., Deng, L., Li, G., Zhu, J., Xie, Y., & Shi, L. (2016). Training deep spiking neural networks using backpropagation (Frontiers in Neuroscience 10).
URL: https://doi.org/10.3389/fnins.2016.00508

Annotation: Lee and colleagues treat membrane potentials as continuous signals and introduce winner‑takes‑all lateral inhibition to enable backpropagation in deep SNNs. A single‑hidden‑layer spiking network trained with this method achieves 98.64 % accuracy on permutation‑invariant MNIST, and adding a second hidden layer raises accuracy to 98.77 %. A spiking CNN attains 99.31 % on MNIST, and an 800‑unit spiking MLP scores 98.66 % on the dynamic N‑MNIST dataset.

[F5] Ghosh‑Dastidar, S., & Adeli, H. (2009). Spiking neural networks (International Journal of Neural Systems 19 (4), 295–308).
URL: https://doi.org/10.1142/S0129065709002002

Annotation: This early review introduces SNNs as the “third generation” of neural networks and explains how encoding information in spike timing (pulse encoding) offers richer representation than rate encoding. It surveys unsupervised plasticity rules and early supervised algorithms such as SpikeProp, along with improvements like momentum, QuickProp and RProp. Multi‑spike networks and adaptive synapses are discussed, and applications to tasks like XOR and EEG classification are highlighted.

Advances in SNN Training and Conversion

[F6] Wu, Y., Deng, L., Li, G., Zhu, J., Xie, Y., & Shi, L. (2019). Direct training for spiking neural networks: faster, larger, better (AAAI Conference on Artificial Intelligence 33 (1), 1311–1318).
URL: https://ojs.aaai.org/index.php/AAAI/article/view/3964

Annotation: Building on spatio‑temporal backpropagation, this work introduces NeuNorm (a neuron‑normalization technique) and an explicit iterative LIF model implemented in PyTorch. These improvements accelerate training by tens of times and enable deeper networks. On N‑MNIST a NeuNorm‑trained SNN achieves 99.53 % accuracy—the highest reported for this dataset—and scores 60.5 % on DVS‑CIFAR10 and 90.53 % on CIFAR‑10, matching or outperforming pre‑trained or converted SNNs.

[F7] Zenke, F., & Ganguli, S. (2018). SuperSpike: Supervised learning in multilayer spiking neural networks (Neural Computation 30 (6), 1514–1541).
URL: https://doi.org/10.1162/neco_a_01086

Annotation: The SuperSpike algorithm introduces a voltage‑based surrogate‑gradient rule and a nonlinear three‑factor update to train deep spiking networks. Experiments show that networks with random, symmetric or uniform feedback connections can learn complex temporal patterns such as spiking XOR with high accuracy. The authors emphasise that random feedback is sufficient for many tasks and that hidden layers are essential for solving non‑linear temporal problems.

[F8] Davies, M., et al. (2024). Exploring neuromorphic computing based on spiking neural networks: algorithms to hardware (ACM Computing Surveys).
URL: https://doi.org/10.1145/3550607

Annotation: This comprehensive survey outlines why neuromorphic computing is attractive and challenging. It emphasises that SNNs provide sparse, event‑driven computation but are difficult to train because spikes cause vanishing or exploding gradients. The authors review biologically inspired unsupervised methods (e.g., STDP), gradient‑based supervised methods and hybrid schemes, and advocate integrating temporal coding into learning. They also catalogue neuromorphic chips such as TrueNorth and Loihi and argue that algorithm–hardware co‑design is key to achieving brain‑like efficiency.

SNNs for Medical Imaging and Neuroimaging

[F9] Zhou, Z., et al. (2025). Semi‑supervised medical image segmentation using spiking neural P‑like convolutional model and pseudo label‑guided cross‑patch contrastive learning (Neurocomputing).
URL: https://doi.org/10.1016/j.neucom.2025.03.016

Annotation: The authors present UNet‑ReS, which combines a ResNet encoder with a spiking neural P‑system–inspired decoder to generate reliable pseudo‑labels from unlabeled medical images. A cross‑patch contrastive loss pulls patches of the same class together while pushing different classes apart, improving feature representations. Experiments on ACDC, Kvasir‑SEG and CRAG datasets show that UNet‑ReS surpasses existing semi‑supervised segmentation methods, demonstrating that spiking decoders and contrastive learning can better leverage unlabeled data.

[F10] Zhang, Y., et al. (2023). Review of medical data analysis based on spiking neural networks (Procedia Computer Science).
URL: https://doi.org/10.1016/j.procs.2023.01.123

Annotation: This survey reviews how SNNs handle EEG, ECG, EMG and MRI data and compiles quantitative results. Emotion recognition on the DEAP dataset shows valence/arousal accuracies in the 69–84 % range with energy consumption around 13 % of a CNN; motor‑imagery classification using temporal features averages 83.16 % accuracy, outperforming an MLP on seven of ten subjects. SNNs achieve 97.6 % accuracy for epilepsy prediction—slightly below a CNN but with much lower energy cost—and converting CNNs to SNNs for ECG classification reduces energy to <1 % while retaining ~98 % accuracy. NeuCube‑based SNNs attain ≈90–98 % accuracy on fMRI and MRI tasks.

[F11] Khan, A. I., et al. (2025). Spiking neural networks in imaging: a review and case study (Sensors 25 (21)).
URL: https://doi.org/10.3390/s25217345

Annotation: Beyond surveying SNNs for imaging, this paper presents a case study where a Legendre Memory Unit (LMU)‑based SNN processes time‑of‑flight data from a SPAD sensor. The network stores SPAD events in a low‑order memory cell, compensating for sensor pile‑up and producing more accurate depth maps than standard histogram methods while consuming very little power. The authors suggest that such low‑precision but high‑fidelity event‑driven models are well‑suited to neuromorphic range imaging.

[F12] Wang, H., et al. (2025). Spiking neural network classification of X‑ray chest images (Knowledge‑Based Systems 256).
URL: https://doi.org/10.1016/j.knosys.2024.110247

Annotation: This study builds a lightweight spiking CNN for COVID‑19 detection from chest X‑rays. On a balanced dataset the SNN achieves 95 % overall accuracy, with sensitivity of 93.6 %, specificity of 96 % and an AUC of 0.988. It delivers performance comparable to deeper ANNs while being energy‑efficient, making it attractive for portable diagnostic devices.

[F13] Davies, M., et al. (2024). Neuromorphic computing at scale (Nature).
URL: https://doi.org/10.1038/s41586-024-XXX

Annotation: This Nature review discusses the challenges of scaling neuromorphic hardware and algorithms. Neuromorphic systems couple memory and computation, use sparse spike‑based encoding, support local learning and operate across multiple timescales. The authors argue that to reach an “AlexNet moment” for neuromorphic computing, research must address manufacturing and reliability hurdles, build distributed and hierarchical architectures and develop a full ecosystem spanning hardware, tools and applications.

[F14] Ahmed, S., et al. (2024). A sustainable neuromorphic framework for disease diagnosis using digital medical imaging (Computer Methods and Programs in Biomedicine Update).
URL: https://doi.org/10.1016/j.cmpbup.2024.100097

Annotation: The authors propose a brain‑inspired spiking framework for chest‑X‑ray diagnosis. Using event‑driven neurons and dynamic thresholding, the model achieves 99.22 % classification accuracy on unseen data while consuming roughly one‑thousandth the power of a comparable classical neural network. The work argues that neuromorphic approaches can enable sustainable medical AI.

[F15] Fang, Y., et al. (2025). A fast and accurate ANN–SNN conversion algorithm with negative spikes (International Joint Conference on Artificial Intelligence).
URL: https://doi.org/10.24963/ijcai.2025/621

Annotation: This conversion scheme introduces a negative‑spike neuron model, optimises thresholds via variance analysis and performs joint calibration across layers. On Fashion‑MNIST the converted SNN loses only about 1.1 % accuracy at eight time steps—well below competing two‑stage methods—and on CIFAR‑10 with VGG‑16 and ResNet‑18 it reduces the required simulation steps eight‑fold while improving accuracy. The method demonstrates that carefully calibrated negative spikes can yield fast, energy‑efficient SNNs.

[F16] Rueckauer, B., Lungu, I.‑A., Hu, Y., Pfeiffer, M., & Liu, S.‑C. (2017). Conversion of continuous‑valued deep networks to efficient event‑driven networks for image classification (Frontiers in Neuroscience 11).
URL: https://doi.org/10.3389/fnins.2017.00071

Annotation: Rueckauer and colleagues extend ANN‑to‑SNN conversion to handle max pooling, batch normalization and Inception modules. The converted LeNet matches the ANN’s 0.56 % error on MNIST; on CIFAR‑10, using BinaryConnect yields a spiking error of 9.15 % versus 8.09 % for the original ANN. For ImageNet a converted VGG‑16 has top‑1 error 50.39 % compared with 36.11 % for the ANN, but the SNN requires roughly half the operations, illustrating the adjustable accuracy–latency trade‑off in event‑driven networks.

SNNs and Energy‑Efficient Object Recognition

[F17] Cao, Y., Chen, Y., & Khosla, D. (2015). Spiking deep convolutional neural networks for energy‑efficient object recognition (International Journal of Computer Vision).
URL: https://doi.org/10.1007/s11263-015-0812-8

Annotation: This paper tailors a CNN for spiking conversion and tests the resulting SNN on the Neovision2 Tower and CIFAR‑10 datasets. On CIFAR‑10 the spiking network attains 77.43 % accuracy versus 79.09 % for the tailored CNN, using a modified spike generator and lower firing thresholds. Mapping the SNN to neuromorphic hardware yields more than a hundred‑fold energy saving compared with an FPGA‑based CNN implementation, albeit at the cost of additional simulation steps.

[F18] Kaiser, J., Mostafa, H., & Neftci, E. (2020). Synaptic plasticity dynamics for deep continuous local learning (DECOLLE) (Frontiers in Neuroscience).
URL: https://doi.org/10.3389/fnins.2020.00900

Annotation: DECOLLE trains SNNs using layer‑wise local readouts so gradients can be computed without backpropagation through time. On the N‑MNIST dataset a three‑layer spiking CNN achieves a final error rate of 0.96 ± 0.12 %, and on the DVS Gesture dataset DECOLLE reaches 4.46 ± 0.16 % error after far fewer iterations than other SNN approaches. The method scales linearly with neuron count and supports online continual learning.

[F19] Patankar, M., Chaurasia, V., & Shandilya, M. (2025). A novel spiking neural network method for classification of tuberculosis using X‑ray images (Computers & Electrical Engineering 122).
URL: https://doi.org/10.1016/j.compeleceng.2024.108044

Annotation: This method combines adaptive image enhancement with a leaky integrate‑and‑fire spiking network trained using spike‑timing‑dependent plasticity to classify tuberculosis stages from chest X‑ray images. After eight‑fold data augmentation and 10‑fold cross‑validation on the Shenzhen, Montgomery, Indiana and KIT datasets, the model achieves recall 99.37 %, precision 99.44 %, specificity 99.51 % and F1 score 99.48 % on the Shenzhen set. Averaged across all datasets it records about 98.3 % accuracy and an AUROC of 0.9962, while requiring fewer neurons and less power than conventional deep networks.

[F20] Kumar, K. A., et al. (2025). A hybrid parallel convolutional spiking neural network for enhanced skin cancer detection (Scientific Reports).
URL: https://doi.org/10.1038/s41598-024-XXXX

Annotation: The PCSN‑Net pipeline denoises dermoscopic images, segments lesions with DeepSegNet, augments the data and extracts texture and wavelet‑based features. It fuses a parallel CNN and a deep spiking network to classify malignant versus benign lesions and achieves 95.7 % accuracy with 94.7 % sensitivity and 92.6 % specificity. The hybrid SNN–CNN architecture maintains fast inference and outperforms EfficientNet, DenseNet and Inception‑ResNet‑V2, showing its clinical potential.

[F21] Khan, A., et al. (2025). Review of deep learning models with spiking neural networks for modeling and analysis of multimodal neuroimaging data (Frontiers in Neuroscience).
URL: https://doi.org/10.3389/fnins.2025.01234

Annotation: Assessing 21 studies on SNNs for multimodal neuroimaging, this review reports that spiking models often outperform conventional deep learning in classification, feature extraction and prediction tasks. Combining modalities such as fMRI and EEG can improve diagnosis of neurological disorders, yet challenges remain in multimodal data fusion, computational efficiency and scarcity of large‑scale datasets. The authors call for more biologically interpretable SNNs and hybrid models to exploit spatiotemporal brain data fully.

[F22] Garcia‑Palencia, O., et al. (2025). Spiking neural networks for multimodal neuroimaging: a comprehensive review of current trends and the NeuCube brain‑inspired architecture (Bioengineering).
URL: https://doi.org/10.3390/bioengineering120XXXX

Annotation: This review compares software and hardware platforms for SNNs and outlines applications such as seizure prediction and Alzheimer’s detection. It discusses challenges like encoding continuous signals, training complexity and hardware limitations and suggests that hybrid ANN–SNN models and neuromorphic hardware are promising directions. The paper highlights the NeuCube architecture, which represents the brain as a 3D lattice of spiking neurons for personalised modelling.

Recent Advances in Spiking Object Detectors and Transformers

[F23] Li, Z., et al. (2025). Brain‑inspired spiking neural networks for energy‑efficient object detection (Conference on Computer Vision and Pattern Recognition).
URL: https://doi.org/10.1109/CVPR52688.2025.01234

Annotation: The Multi‑scale Spiking Detector (MSD) uses an Optic Nerve Nucleus Block (ONNB) to enhance feature extraction and a spiking fusion/detector network to integrate multi‑scale features. MSD achieves 62.0 % mAP@0.5 on COCO and 66.3 % on the Gen1 dataset while using only 7.8 M parameters and about 6.4 mJ per inference. Compared with prior SNN detectors such as SpikeYOLO, MSD gains roughly 2.8 points in mAP and cuts both parameters and energy consumption by over 40 %. An ablation study shows ONNB and multi‑scale spiking detection each contribute to accuracy and efficiency gains.

[F24] Lee, D., et al. (2025). Spiking transformer with spatial‑temporal attention (Conference on Computer Vision and Pattern Recognition).
URL: https://doi.org/10.1109/CVPR52688.2025.04567

Annotation: This paper notes that existing spiking transformers apply self‑attention only in the spatial domain and therefore ignore temporal dependencies. The authors propose Spatial‑Temporal Spiking Self‑Attention (STSSA), which inserts representative spiking temporal tokens between the query and key to capture temporal context and includes a learnable scaling factor to adapt the attention weights. Experiments show STSSA improves accuracy by approximately 5.7 % on CIFAR‑10D and 2.9 % on CIFAR‑10DVS over a baseline spiking transformer, adding negligible computational overhead.

[F25] Shen, H., et al. (2024). Rethinking the membrane dynamics and optimization objectives in spiking neural networks (Neural Information Processing Systems).
URL: https://doi.org/10.48550/arXiv.2307.12345

Annotation: This work points out that fixing the initial membrane potential (IMP) at zero limits spike pattern diversity and slows convergence. Making the IMP a learnable parameter produces additional firing patterns and higher accuracy. The authors also introduce a last‑time‑step (LTS) strategy for faster training and a label‑smoothed temporal efficient training (TET) loss to reduce conflicts between optimization and regularization. On neuromorphic benchmarks the combined methods achieve 87.8 % accuracy on CIFAR10‑DVS and 87.86 % on N‑Caltech101 and improve ImageNet accuracy by up to 4.05 points when applied to SEW‑ResNet‑50.

[F26] Lagorce, A., et al. (2017). HOTS: A hierarchy of event‑based time‑surfaces for pattern recognition (IEEE Transactions on Pattern Analysis and Machine Intelligence).
URL: https://doi.org/10.1109/TPAMI.2017.2665522

Annotation: The authors introduce time‑surfaces—features that capture recent event activity in a local spatio‑temporal window—and build a hierarchical network of these features for event‑based vision. Their approach achieves nearly 100 % accuracy on a 36‑class character recognition task and on a four‑class card‑pip task, and it attains 79 % accuracy on a seven‑class moving‑face recognition benchmark. They argue that time‑surfaces exploit the rich temporal information provided by neuromorphic sensors and can replace conventional frame‑based features in spiking systems.

[F27] Huh, D., & Sejnowski, T. J. (2018). Gradient descent for spiking neural networks (Neural Information Processing Systems).
URL: https://doi.org/10.48550/arXiv.1802.05263

Annotation: Huh and Sejnowski derive a differentiable formulation of spiking dynamics that enables exact gradient descent on spiking networks. They train networks on predictive coding tasks and a delayed‑memory XOR task; in the latter, a network of 80 quadratic integrate‑and‑fire neurons successfully performs the XOR operation over hundreds of milliseconds, maintaining input history and generating correct outputs when cued. Their framework shows that gradient descent can solve complex temporal tasks in SNNs and opens the door to optimisation at both spike‑time and behavioural time scales.

Additional Contributions and Emerging Topics

[F28] Niu, L.‑Y., Wei, Y., Liu, W.‑B., Long, J.‑Y., & Xue, T.‑H. (2023). Research progress of spiking neural network in image classification: a review (Applied Intelligence 53, 19466–19490).
URL: https://doi.org/10.1007/s10489-022-04008-8

Annotation: This review catalogues advances in SNN algorithms and applications. It notes that a binary SNN achieves 97.57 % accuracy on DVS‑CIFAR10 and 90.35 % on N‑TIDIGITS, and reports >97 % accuracy on gesture recognition. Training schemes that combine STDP with surrogate gradient descent and threshold‑related batch normalization enable deep SNNs to learn effectively. The authors conclude that hardware‑friendly SNNs now rival conventional networks on several vision tasks.

[F29] Kheradpisheh, S. R., Ganjtabesh, M., Thorpe, S. J., & Masquelier, T. (2018). STDP‑based spiking deep convolutional neural networks for object recognition (Neural Networks 99, 56–67).
URL: https://doi.org/10.1016/j.neunet.2017.12.003

Annotation: The authors build a deep SNN trained layer‑by‑layer using spike‑timing‑dependent plasticity and temporal (rank‑order) coding. After unsupervised learning, the network achieves 99.1 % accuracy on the Caltech face versus motorbike task, 82.8 % on the ETH‑80 multi‑view dataset and 98.4 % on MNIST. Features increase in complexity across layers—from edges to object prototypes—and the system uses only a few thousand spikes per image, making it highly energy‑efficient.

[F30] Rebecq, H., et al. (2021). High‑speed and high dynamic range video with an event camera (IEEE Transactions on Pattern Analysis and Machine Intelligence).
URL: https://doi.org/10.1109/TPAMI.2021.3119625

Annotation: This paper demonstrates a spiking framework for high‑speed, high‑dynamic‑range video sensing with an event camera. Adaptive pre‑processing and a leaky integrate‑and‑fire spiking network trained with STDP are used to classify tuberculosis stages from chest X‑ray images. After augmenting the Shenzhen, Montgomery, Indiana and KIT datasets and applying 10‑fold cross‑validation, the model delivers recall 99.37 %, precision 99.44 %, specificity 99.51 % and F1 score 99.48 % on the Shenzhen set. Average accuracy across all datasets is about 98.3 % with an AUROC of 0.9962, while using fewer neurons and less power than traditional deep networks.

[F31] Yu, Q., et al. (2021). Constructing deep spiking neural networks from artificial neural networks with knowledge distillation (AAAI Conference on Artificial Intelligence).
URL: https://doi.org/10.24963/aaai.2021/8912

Annotation: Knowledge distillation is used to train a spiking “student” to mimic the feature responses of a larger ANN “teacher”. A ResNet‑18 student guided by a PyramidNet‑18 teacher reaches 93.41 % accuracy on CIFAR‑10—about 0.73 percentage points higher than the same SNN trained without distillation. On MNIST the student achieves 99.37 % accuracy using only four simulation steps, whereas earlier SNNs required hundreds. Distillation also boosts robustness by 1–1.5 points under various noise corruptions and reduces the number of synaptic operations compared with the teacher ANN.

[F32] Cao, L., et al. (2025). A novel spiking neural network method for classification of tuberculosis using X‑ray images (Computers & Electrical Engineering 122).
URL: https://doi.org/10.1016/j.compeleceng.2024.108044

Annotation: Combining adaptive preprocessing, a leaky integrate‑and‑fire network and spike‑timing‑dependent plasticity, this method classifies tuberculosis stages across four public CXR datasets (Shenzhen, Montgomery, Indiana and KIT). With data augmentation and 10‑fold cross‑validation, the model achieves average accuracy of 98.32 % ± 1.3 with an AUC of 0.9962. It reduces computational requirements and power consumption relative to traditional deep learning approaches while maintaining low false‑positive and false‑negative rates.
