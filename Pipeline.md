###  **Objective**

To build a **spontaneous emotional speech corpus** in **Tunisian Arabic dialect** from broadcast media, annotated with **categorical** and **dimensional (VAD)** emotion labels, while ensuring **data anonymization** and **high-quality standards**.

---

### 1. **Selection of Broadcast Materials**

* **Sources**: Tunisian broadcast content retrieved from **YouTube**, including:

  * TV shows
  * Debates
  * Interviews

* **Covered domains**:

  * Sport
  * Politics
  * Culture
  * Society

* **Linguistic criteria**:

  * Only **spontaneous speech** in **Tunisian dialect** was included.

* **Legal Note**:

  > *In Tunisia, it is possible to make fair use of copyrighted materials according to **Article 10** of **Law No. 94-36** (February 24, 1994), on literary and artistic property, as amended by **Law No. 2009-33** (June 23, 2009).*

* **Corpus statistics**:

  * **3,793 recordings**
  * Durations ranging from **1.15 seconds to 10.97 minutes**
  * **1,259 unique speakers**

---

### 2. **Segment Extraction and Preprocessing**

* **Tool used**: [**WavePad**](https://www.nch.com.au/wavepad/index.html)

* **Steps**:

  * Manual listening of raw broadcasts
  * Selection of speech segments with **audible emotional content**
  * **Silence trimming**: All silences exceeding **2 seconds** were shortened to **2 seconds**
  * **Manual anonymization**: Personal data (names, places) were replaced with **silence**

* **Audio specifications**:

  * Format: `.wav`
  * Sampling rate: **44.1 kHz**
  * Average segment duration: **\~20 seconds**

---

### 3.  **Emotion Annotation**

#### 🔹 **Dimensional Annotation** *(Valence, Arousal, Dominance)*

* **Tool used**: [**CARMA**](https://carma-app.github.io/), based on FeelTrace

* **Dimensions**:

  * **Valence** (0 = very negative → 10 = very positive)
  * **Arousal** (0 = very passive → 10 = very active)
  * **Dominance** (0 = very submissive → 10 = very dominant)

* **Custom configuration**:

  * Initial value: **5** (neutral)
  * Real-time annotation using **mouse or keyboard arrows**
  * Annotators see their own trajectory as a live curve
  * Annotation was **only applied to segments ≥ 10 seconds** to reduce bias due to reaction delays
  * **Annotation sampling rate**: Every **0.25 seconds** (i.e., 4 values per second)

* **Final score**:

  > For each segment and axis, the final value corresponds to the **mean of the annotation curve** across the entire duration.

* **Total annotated duration**: Over **23 hours** across the corpus

---

#### 🔹 **Categorical Annotation** *(Manual, Majority Voting)*

* **Emotion categories**:

  * **Anger**, **Joy**, **Sadness**, **Neutral**, **Disgust**, **Satisfaction**
* **Method**:

  > Each segment was labeled according to the **majority vote** among the three annotators.

---

### 4. **Annotators**

* **Number**: **3 annotators** (2 women, 1 man)
* **Age range**: **27–31 years**
* **Profile**:

  * Native speakers of **Tunisian dialect**
  * Graduates of the **Faculty of Arts and Humanities**
  * Experienced in **sentiment analysis**
* **Quality assurance**:

  * Annotators were selected following a **review of their previous work** and **qualifications**
  * **Training sessions** and **annotation guides** were provided
  * **Consensus meetings** were held to ensure consistent interpretation and reduce subjectivity
