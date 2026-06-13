# Session 3 : Interpretation & Presentation
## 1. Interpret PC
<img width="219" height="778" alt="image" src="https://github.com/user-attachments/assets/2685932f-3292-43d1-8684-5d819eea741e" />

### 1. PC1 Loading
- Annual Return: 0.298 
- Excess Return: 0.318
- Systematic Risk: -0.236
- Total Risk: -0.187
- Abs.Win Rate: 0.299
- Rel.Win Rate: 0.305

#### 1.1 PC1 Interpretation
PC1 represents overall portfolio performance.
Portfolios with higher PC1 scores tend to have higher returns and winning rates while exhibiting lower risk.

### 2. PC2 Loading
- Annual Return: 0.267
- Excess Return: 0.200
- Systematic Risk: 0.308
- Total Risk: 0.410
- Abs.Win Rate: 0.004
- Rel.Win Rate: -0.036

#### 2.1 PC2 Interpretation
PC2 represents portfolio risk.
Portfolios with higher PC2 scores tend to have greater systematic and total risk.


## 2. Interpret Clusters by Local SHAP method

### How to Read the SHAP Plot
- SHAP value > 0: increases the probability of belonging to the selected cluster
- SHAP value < 0: decreases the probability of belonging to the selected cluster
- Red points: high feature values
- Blue points: low feature values
- Feautures at the top have a greater influence on cluster classification
- The farther a point is from zero, the stronger its impact on the model's prediction


### 1. Cluster #1
<img width="645" height="311" alt="image" src="https://github.com/user-attachments/assets/4c0f813c-a316-4bfe-8b29-6f3d7006cff0" />

#### 1.1 Cluster #1 Interpretation
- Total Risk: Lower total risk increases the probability of belonging to Cluster #1.
- Systematic Risk: Lower systematic risk increases the probability of belonging to Cluster #1.
- Annual Return: Higher annual return increases the probability of belonging to Cluster #1.
- Relative Win Rate: Higher relative win rate increases the probability of belonging to Cluster #1.
- Excess Return: Higher excess return increases the probability of belonging to Cluster
- Absolute Win Rate: Higher absolute win rate increases the probability of belonging to Cluster #1.


### 2. Cluster #2
<img width="630" height="309" alt="image" src="https://github.com/user-attachments/assets/437122dc-afc8-414c-8d90-ddbc7b9a391e" />

#### 2.1 Cluster #2 Interpretation
- Annual Return: Lower annual return increases the probability of belonging to Cluster #2.
- Excess Return: Lower excess return increases the probability of belonging to Cluster #2.
- Relative Win Rate: Lower relative win rate increases the probability of belonging to Cluster #2.
- Absolute Win Rate: Lower absolute win rate increases the probability of belonging to Cluster #2.
- Systematic Risk: Has a relatively small influence on Cluster #2.
- Total Risk: Has a relatively small influence on Cluster #2.

### 3. Cluster #3
<img width="621" height="311" alt="image" src="https://github.com/user-attachments/assets/28c9db36-7ab9-43d6-b484-383c5d58c53e" />

#### 3.1 Cluster #3 Interpretation
- Total Risk: Higher total risk strongly increases the probability of belonging to Cluster #3.
- Systematic Risk: Higher systematic risk strongly increases the probability of belonging to Cluster #3.
- Relative Win Rate: Lower relative win rate increases the probability of belonging to Cluster #3.
- Annual Return: Higher annual return slightly increases the probability of belonging to Cluster #3.
- Absolute Win Rate: Lower absolute win rate increases the probability of belonging to Cluster #3.
- Excess Return: Higher excess return slightly increases the probability of belonging to Cluster #3.


### 4. Cluster #4
<img width="612" height="308" alt="image" src="https://github.com/user-attachments/assets/54377fb9-4ba3-4988-b30c-73f12082b55e" />

#### 4.1 Cluster #4 Interpretation
- Annual Return: Higher annual return strongly increases the probability of belonging to Cluster #4.
- Total Risk: Higher total risk increases the probability of belonging to Cluster #4.
- Excess Return: Higher excess return increases the probability of belonging to Cluster #4.
- Relative Win Rate: Higher relative win rate increases the probability of belonging to Cluster #4.
- Systematic Risk: Higher systematic risk increases the probability of belonging to Cluster #4.
- Absolute Win Rate: Higher absolute win rate slightly increases the probability of belonging to Cluster #4.


## 3. Labeling Each Cluster & Summary of Each Characteristics

### 1. Cluster #1 : "Efficient Low-Risks Portfolios"
- Total Risk ↓
- Systematic Risk ↓
- Annual Return ↑
- Excess Return ↑
- Rel. Win Rate ↑
- Abs. Win Rate ↑

This cluster is characterized by high returns and strong winning rates while maintaining relatively low risk. This suggests an efficient portfolio that balances performance and stability.

### 2. Cluster #2 : "Underperforming Portfolios"
- Annual Return ↓↓
- Excess Return ↓↓
- Rel. Win Rate ↓
- Abs. Win Rate ↓
- Systematic Risk (weak effect)
- Total Risk (weak effect)

This cluster is mainly characterized by low returns and low winning rates. The SHAP plot shows that low Annual Return, low Excess Return, low Relative Win Rate, and low Absolute Win Rate push portfolios toward this cluster. Risk variables appear less influential for this cluster.

### 3. Cluster #3 : "High-Risk Portfolios"
- Total Risk ↑↑
- Systematic Risk ↑↑
- Rel. Win Rate ↓
- Annual Return ↑
- Abs. Win Rate ↓
- Excess Return ↑

This cluster is characterized by very high systematic risk and total risk, while having relatively low winning rates. Although returns can be moderately high, risk is the dominant factor that distinguishes this cluster.

### 4. Cluster #4 : "Aggressive Growth Portfolios"
- Annual Return ↑↑
- Excess Return ↑
- Abs. Win Rate ↑
- Rel. Win Rate ↑
- Systematic Risk ↑
- Total Risk ↑

This cluster is characterized by high returns, high excess returns, and strong winning rates. Although the cluster also has relatively high risk, its strong performance indicators suggest an aggressive growth-oriented portfolio.


## 4. Discussion & Limitation
### Discussion
The clustering analysis identified four distinct portfolio groups based on six performance indicators. When I run the random forest model, it achieved a testing accuracy of 94.7%. It indicates that the identified clusters are well separated. Feature importance analysis showed that 'Annual Return' was the most important variable for distinguishing portfolio groups, followed by Total Risk, Excess Return, and Systematic Risk. This indicates that portfolio performance is primarily differentiated by return characteristics, while risk measures also contribute significantly to cluster formation. Overall, the results support the idea that portfolio evaluation should consider both return and risk rather than just a single performance measure.

### Limitations & Reflection
#### Limitations
1. Small dataset size
One limitation of this study is the relatively small number of portfolio observations. Some clusters contained only a few portfolios and it may reduce the stability and generalizability of the clustering results.

2. PCA visualization limitation
PCA was used to visualize six-dimensional portfolio data in a two-dimensional space. While PCA makes cluster patterns easier to interpret, some information is inevitably lost during dimensionality reduction.

3. Interpretation challenge
A major challenge of this project was interpreting clusters that were created using six performance indicators simultaneously. Since K-means groups portfolios based on overall similarity across all variables, the meaning of each cluster was not immediately obvious. To address this issue, cluster means, feature importance, and local SHAP analyses were used together to better understand the characteristics of each portfolio group.

#### Reflection
One challenge of this project was selecting appropriate variables for clustering and interpreting the resulting clusters. Instead of using all variables in the dataset, I selected six performance indicators (Annual Return, Excess Return, Systematic Risk, Total Risk, Absolute Win Rate, and Relative Win Rate) based on the methodology of the paper. These indicators were chosen because they directly represent portfolio performance from return, risk, and consistency perspective.

Another challenge was visualizing and interpreting six-dimensional portfolio data. Since it is impossible to directly visualize six variables at the same time, PCA was applied to reduce the data into two principal components. The PCA biplot showed that PC1 was mainly associated with return and winnig-rate variables, while PC2 was mainly associated with risk variables. In addition, PC1 and PC2 together explained approsimately 64.7% of the total variance (41.13% +23.53%), suggesting in the original six variables. Therefore, PC1 and PC2 were considered sufficient for visualizing and interpreting portfolio patterns.

To further improve interpretability, cluster means, random forest feature importance, and local SHAP explanations were used together. Combining these methods made it possible to understand not only how portfolios were grouped, but also why each cluster was formed and which performance indicators contributed most to the clustering results.
