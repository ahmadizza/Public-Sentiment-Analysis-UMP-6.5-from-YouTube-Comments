# **Sentiment Analysis on the 6.5% Increase of Indonesia’s Provincial Minimum Wage (UMP)**

## **1. Introduction**

The Provincial Minimum Wage (UMP) is a crucial economic policy that directly impacts both workers and employers in Indonesia. In the current year, the government announced a 6.5% increase in the UMP, triggering widespread public discussion. Reactions vary from strong support to criticism, especially across social media platforms such as YouTube. Understanding these reactions can offer insights into public sentiment toward the policy and its socio-economic implications.

## **2. Data Source**

The dataset consists of comments collected from 50 YouTube videos related to the UMP 6.5% increase. Selected videos include official news reports, public discussions, economic analyses, and commentary from content creators covering the topic.

---

## **3. Data Preprocessing**

### **3.1 Duplication Check**

Duplicate comments were removed to ensure data integrity.

### **3.2 Manual Sentiment Labeling**

Manual labeling was performed before text preprocessing to preserve the original sentiment context. Labels:

* 1.0 = Negative
* 2.0 = Neutral
* 3.0 = Positive

The label column was then converted into the appropriate data type.

### **3.3 Handling Missing Values**

No missing values were found in the dataset.

### **3.4 Text Cleaning**

Cleaning included:

* Lowercasing text
* Removing URLs
* Removing mentions (@username)
* Removing numbers
* Removing special characters
* Removing excessive whitespace

### **3.5 Normalization**

Slang words and typos were normalized using a custom dictionary to convert them into formal vocabulary.

### **3.6 Stopwords Removal**

Indonesian stopwords were removed to retain meaningful terms.

### **3.7 Lemmatization**

Words were reduced to their base forms to improve uniformity for further analysis.

---

## **4. Exploratory Data Analysis**

### **4.1 Label Distribution**

* Negative (1.0): 861 comments (58%)
* Neutral (2.0): 412 comments (28%)
* Positive (3.0): 214 comments (14%)

Sentiment distribution indicates that negative reactions dominate discussions related to the UMP increase.

### **4.2 Word Clouds**

Word clouds for each sentiment category highlight the following patterns:

* **Overall:** Mixed concerns about wages, job security, prices, and taxes.
* **Negative:** Fear of rising prices, layoffs (PHK), and pressure on small businesses.
* **Neutral:** Focus on wage impact, business conditions, and regional differences.
* **Positive:** Expressions of gratitude, optimism for better welfare, and support for policymakers.

### **4.3 Text Length Analysis**

Negative comments tend to be longer and more varied, while neutral and positive comments are generally shorter and more consistent.

### **4.4 Top 10 Bigrams**

Frequent bigrams include:

* "terima kasih"
* "naik gaji"
* "naik upah"
* "daya beli"
* "harga barang"
* "gaji buruh"
* "upah buruh"
* "lapang kerja"
* "pegawai negeri"
* "upah minimum"

These bigrams reveal discussions focused on wage impact, cost of living, labor conditions, and economic concerns.

---

## **5. Topic Modeling**

### **Topic Distribution**

The dataset forms three main topics with relatively balanced distribution, suggesting recurring themes across discussions.

### **Topic Results**

**Topic 1:**
Positive sentiment and appreciation toward the wage increase. Keywords suggest acknowledgment of policymakers while noting concerns about rising taxes (PPN 12%).

**Topic 2:**
Concerns about layoffs, business pressure, and impacts on labor groups. Discussions emphasize broad effects on workers and small entrepreneurs.

**Topic 3:**
Similar to Topic 2 but with focus on wages, business challenges, small shops, and implications for micro- and medium-sized enterprises, including mentions of UMR/UMP differences.

---

## **6. Modeling**

### **6.1 Oversampling**

Oversampling was performed to balance the classes:

* Negative: 412
* Neutral: 412
* Positive: 412

This ensures fair learning across sentiment categories.

### **6.2 SVM Classification**

SVM achieved:

* Accuracy: 73%
* F1-Positive: 0.87
* F1-Negative: 0.71
* F1-Neutral: 0.62

The model performs best on Positive and Negative classes but struggles with Neutral sentiment. Improved feature engineering or model tuning may address this limitation.

---

## **7. Recommendations**

* Provide clearer public communication on the benefits of the wage increase.
* Offer support programs for small businesses to adapt to higher labor costs.
* Monitor economic indicators such as prices, layoffs, and business performance.
* Improve general worker welfare beyond wage increases.
* Maintain transparency regarding policy implementation and its impacts.
* Conduct further research on region-based sentiment trends.

---

## **8. Conclusion**

Public reactions to the 6.5% UMP increase are diverse. While some citizens welcome the policy as a step toward improving worker welfare, many express anxiety about rising prices, potential layoffs, and pressures on businesses. References to political figures and specific regions indicate that perceptions may also be influenced by socio-political factors. With careful implementation and monitoring, the policy can yield positive outcomes, provided concerns from multiple stakeholders are addressed.
