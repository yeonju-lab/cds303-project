# Session 3 : Interpretation & Presentation
## 1. Interpret PC
<img width="221" height="773" alt="image" src="https://github.com/user-attachments/assets/f7a518ae-e7d7-4439-9af2-81ab0e6596c3" />


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
-  Systematic Risk: Lower systematic risk increases the probability of belonging to Cluster #1.
- Annual Return: Higher annual return increases the probability of belonging to Cluster #1.
- Relative Win Rate: Higher relative win rate increases the probability of belonging to Cluster #1.
- Excess Return: Higher excess return increases the probability of belonging to Cluster
- Absolute Win Rate: Higher absolute win rate increases the probability of belonging to Cluster #1.


### 2. Cluster #2
<img width="630" height="309" alt="image" src="https://github.com/user-attachments/assets/437122dc-afc8-414c-8d90-ddbc7b9a391e" />

#### 2.1 Cluster #2 Interpretation
- Annual Return: Higher annual return increases the probability of belonging to Cluster #2.
- Excess Return: Higher excess return increases the probability of belonging to Cluster #2.
- Relative Win Rate: Lower relative win rate increases the probability of belonging to Cluster #2.
- Absolute Win Rate: Lower absolute win rate increases the probability of belonging to Cluster #2.
- Systematic Risk: Higher systematic risk slightly increases the probability of belonging to Cluster #2.
- Total Risk: Higher total risk slightly increases the probability of belonging to Cluster #2.


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
- Annual Return ↑
- Excess Return ↑
- Abs. Win Rate ↑
- Rel. Win Rate ↑
- Systematic Risk ↓
- Total Risk ↓

This cluster achieves strong returns and winning rates while maintaining relatively low risk. It represents efficient portfolios that balance performance and stability.

### 2. Cluster #2 : "Return-Focused Portfolios"
- Annual Return ↑↑
- Excess Return ↑↑
- Abs. Win Rate ↓
- Rel. Win Rate ↓
- Systematic Risk ↑
- Total Risk ↑

This cluster is primarily driven by high returns. Although winning rates are relatively lower, portfolios in this group focus on maximizing performance.

### 3. Cluster #3 : "High-Risk Portfolios"
- Annual Return ↑ (slightly)
- Excess Return ↑ (slightly)
- Abs. Win Rate ↓
- Rel. Win Rate ↓
- Systematic Risk ↑↑
- Total Risk ↑↑

This cluster is dominated by very high risk levels. Risk is the strongest factor associated with this cluster, while winning rates remain relatively low.

### 4. Cluster #4 : "Aggressive Growth Portfolios"
- Annual Return ↑↑
- Excess Return ↑
- Abs. Win Rate ↑
- Rel. Win Rate ↑
- Systematic Risk ↑
- Total Risk ↑

This cluster combines high returns, high winning rates, and higher risk exposure. It represents portfolios pursuing aggressive growth opportunities.
