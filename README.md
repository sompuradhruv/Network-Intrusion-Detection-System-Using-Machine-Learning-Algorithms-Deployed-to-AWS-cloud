# Network Intrusion Detection System (NIDS)

## 1. Problem Statement

### 1.1 Background (System Study Details in Brief)

Network security is a relatively obscure branch of cyber-safety, especially when it comes to the average person. The elderly gentleman across the street cannot be expected to understand why he got a DDoS attack whilst making his routine payment to the milkman. This is where our Intrusion Detection System (IDS) deployed on the cloud comes into play.

Intrusion Detection System (IDS) is a device or software application which monitors network or system activities and identifies any malicious activity. With the outstanding growth and usage of the internet, concerns about how to communicate and protect digital information safely have increased. Hackers use various attacks to obtain valuable information. Many intrusion detection techniques, methods, and algorithms help detect these attacks. The main objective of this project is to detect and prevent network intrusions.

### 1.2 Problem Statement

The increasing frequency and sophistication of cyber threats pose a significant challenge to the security of digital systems. As technology advances, there is a growing need for a robust IDS that can effectively identify and mitigate various forms of malicious activities within networks. The objective of this project is to develop an IDS that detects known intrusion patterns and adapts to evolving cyber threats, ensuring the integrity and security of sensitive data.

### 1.3 Novelty

Our IDS leverages state-of-the-art machine learning algorithms on Amazon SageMaker to fortify network defenses.

**Objective:**
- Detect and prevent a spectrum of attacks.
- Employ a robust set of techniques, methods, and algorithms to identify and thwart potential threats.

**Introduction:**
- Intrusion Detection plays a pivotal role in alerting security administrators to potential threats such as intrusions, attacks, and malware.
- Our IDS diligently monitors for suspicious activities, issuing timely alerts and taking proactive measures.

**Incorporating Machine Learning:**
- Integrated machine learning algorithms on AWS SageMaker enhance the system's ability to discern anomalous activities.
- Continuous learning from patterns and trends ensures adaptation to emerging threats in real-time.

**Benefits:**
1. **Precision in Detection:** Minimizes false positives and ensures precise threat detection.
2. **Adaptability:** Proactive defense mechanism, staying ahead of potential intrusions.
3. **Data-Driven Security:** Provides rich data for bolstering security infrastructure and identifying vulnerabilities.

### 1.4 Dataset

We use the NSL KDD dataset provided by the University of New Brunswick. The dataset is in text format and must be converted to CSV format for processing. Each record has 41 attributes identifying various network packet features, with a label assigned to each packet. The 42nd attribute provides data about 13 labels categorized into 1 for ordinary class and 4 attack-type classes (DoS, Probe, R2L, and U2R).

## 2. Results and Discussion

### 2.1 Implementation Results

After training and testing our IDS model against a large dataset, we achieved the following results with different algorithms:

**Support Vector Machine Algorithm:**
- **DoS (Denial of Service):** Accuracy 99.3%, Precision 99.1%, Recall 99.4%, F-Measure 99.2%
- **U2R (User to Root):** Accuracy 99.6%, Precision 91.0%, Recall 82.9%, F-Measure 84%
- **R2L (Remote to Local):** Accuracy 96.7%, Precision 94.8%, Recall 96.2%, F-Measure 95.5%
- **PROBE:** Accuracy 98.5%, Precision 97%, Recall 98.3%, F-Measure 97%

**Ensemble Algorithm:**
- **DoS (Denial of Service):** Accuracy 99.8%, Precision 99.8%, Recall 99.6%, F-Measure 99.7%
- **U2R (User to Root):** Accuracy 99.7%, Precision 94.3%, Recall 87.3%, F-Measure 91%
- **R2L (Remote to Local):** Accuracy 97.2%, Precision 95.7%, Recall 96.2%, F-Measure 96.1%
- **PROBE:** Accuracy 99.2%, Precision 98.7%, Recall 98.9%, F-Measure 98.8%

**K Nearest Neighbours:**
- **DoS (Denial of Service):** Accuracy 99.7%, Precision 99.6%, Recall 99.6%, F-Measure 99.6%
- **U2R (User to Root):** Accuracy 99.7%, Precision 93.1%, Recall 85.1%, F-Measure 87%
- **R2L (Remote to Local):** Accuracy 96.7%, Precision 95.3%, Recall 95.4%, F-Measure 95.4%
- **PROBE:** Accuracy 99.1%, Precision 98.6%, Recall 98.5%, F-Measure 98.5%

### 2.2 Metrics

We evaluate the performance of the IDS based on the following metrics:
- **Accuracy:** Percentage of correctly classified records over the total number of records.
- **Precision (P):** Percentage of true positives (TP) divided by the number of true positives (TP) and false positives (FP).
- **Recall (R):** Percentage of true positives divided by the number of true positives and false negatives (FN).
- **F-Measure (F):** Harmonic mean of precision and recall.

### 2.3 Results in Table Form

| Algorithm | U2R | R2L | DoS | PROBE |
|-----------|-----|-----|-----|-------|
| **SVM** | 99.6% | 96.7% | 99.3% | 98.5% |
| **Ensemble** | 99.7% | 97.2% | 99.8% | 99.2% |
| **KNN** | 99.7% | 96.7% | 99.7% | 99.1% |

**Precision Scores**

| Algorithm | U2R | R2L | DoS | PROBE |
|-----------|-----|-----|-----|-------|
| **SVM** | 91% | 94.8% | 99.1% | 97% |
| **Ensemble** | 94.3% | 95.7% | 99.8% | 98.7% |
| **KNN** | 93.1% | 95.3% | 99.6% | 98.6% |

**Recall Scores**

| Algorithm | U2R | R2L | DoS | PROBE |
|-----------|-----|-----|-----|-------|
| **SVM** | 82.9% | 96.2% | 99.4% | 98.3% |
| **Ensemble** | 87.3% | 96.2% | 99.6% | 98.9% |
| **KNN** | 85.1% | 95.4% | 99.6% | 98.5% |

**F-Measure Scores**

| Algorithm | U2R | R2L | DoS | PROBE |
|-----------|-----|-----|-----|-------|
| **SVM** | 84% | 95.5% | 99.2% | 97% |
| **Ensemble** | 91% | 96.1% | 99.7% | 98.8% |
| **KNN** | 87% | 95.4% | 99.6% | 98.5% |

### 2.4 Graphs

![Graphs](graphs.png)

### 2.5 Mapping the Results with Problem Statement

Our project addresses critical societal needs by deploying an IDS aimed at enhancing cybersecurity universally, transcending age and gender barriers. It safeguards digital assets, particularly benefiting IT and finance sectors, by thwarting network attacks. Furthermore, it lays the groundwork for secure public services, envisioning a future where individuals can connect to potentially insecure networks without compromising data security.

### 2.6 Comparison with Existing System

To improve our model, we compared it with the model used in the research paper "A Deep Learning Approach for Network Intrusion Detection System" by Quamar Niyaz, Weiqing Sun, Ahmad Y Javaid, and Mansoor Alam. The following table highlights the differences:

| Aspect | Self-Taught Learning | Ensemble Algorithm |
|--------|-----------------------|--------------------|
| **Objective** | Learn feature representation from unlabeled data. | Combine multiple models for improved performance. |
| **Learning Approach** | Deep learning, often involving autoencoders. | Combining multiple base models or learners. |
| **Training Data** | Large collection of unlabeled data (xu). | Labeled data for individual base learners. |
| **Stages** | Two stages: Unsupervised Feature Learning (UFL) and Classification. | Single or multiple stages depending on the ensemble type. |
| **Data Distribution** | Unlabeled and labeled data may come from different distributions. | Labeled data may come from the same distribution. |
| **Feature Learning Method** | Sparse Autoencoder is commonly used. | Various base learners, e.g., decision trees, SVMs, neural networks. |
| **Training Process** | Learns optimal feature representation from unlabeled data through back-propagation. | Trains multiple models independently or sequentially. |
| **Model Diversity** | Focuses on learning diverse and meaningful features from the data
