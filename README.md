# Understand Waiting Time in EIP-1559 Transaction Fee Mechanisms

## Project information
- **Authors**: 
- **Disclaimer**: 
- **Acknowledgments**: 
- **Project Summary**: 
Blockchain enables peer-to-peer transactions in cyberspace without a trusted third party. The rapid growth of Ethereum and smart contract blockchains in general — calls for well-designed Transaction Fee Mechanisms (TFMs) to allocate limited storage and computation resources. However, existing research on TFMs needs to consider the waiting time of transactions, which is essential for both computer security and economic efficiency, though often mentioned in different words, such as latency or market congestion. Integrating data from the Ethereum blockchain and mempool, we explore how two types of shocks affect transaction latency. First, we apply regression discontinuity design (RDD) to study the causal inference of the Merge, the most recent significant upgrade of Ethereum. Our results show that the Merge significantly reduces the long waiting time and market congestion. Then, we apply time series analysis to research the interaction of significant NFT drops and market congestion using Facebook Prophet, an open-source algorithm for generating time-series models. Our analysis reveals that the models could significantly improve the forecast of market congestion by considering NFT drops as a shock. Our study contributes to the interdisciplinary research at the intersection of computer security, distributed systems, market design, causal inferences, and time series analysis. Our findings shed light on a new direction of TFMs that prevent market congestion by efficiently forecasting ex-ante other than the current ex-post treatments. 

## Table of Contents
- [data](https://github.com/sunshineluyao/waiting-time-eip1559/tree/main/data)
- [code](https://github.com/sunshineluyao/waiting-time-eip1559/tree/main/code)
- [figs](https://github.com/sunshineluyao/waiting-time-eip1559/tree/main/figs)



## data
```
data
├── Data Source
│   ├── EthereumETL
│   └── MemopoolGuru
└── Data Product on Kaggle
    ├── Queried Data
    └── Processed Data
```

## code
```
code
├── Data_Analyze
│   ├── Analyze_Data_NFT.ipynb
│   └── Analyze_Data_The_Merge.ipynb
├── Data_Process
│   └── Process_Data.ipynb
└── Data_Query
    ├── Query_Data_EthereumETL_Public.ipynb
    └── Query_Data_MemopoolGuru_Public.ipynb
```

## figs

### Result 1: the merge

#### 1.1. The Waiting Time (delay)

##### Visualizations
- Figure 1
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig1](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig1)
<img src="./figs/merge/fig1.png" alt="drawing" width="800"/>
- Figure 2: 
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig2](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig2)
<img src="./figs/merge/fig2.png" alt="drawing" width="800"/>

- Figure 3: 
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig3](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig3)
<img src="./figs/merge/fig3.png" alt="drawing" width="800"/>
- Figure 4: 
HTML [https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig4](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig4)
<img src="./figs/merge/fig4.png" alt="drawing" width="800"/>

##### Moving Average Smoothing

- Figure 12:

<img src="./figs/merge/fig12.png" alt="drawing" width="800"/>


- Figure 13:
<img src="./figs/merge/fig13.png" alt="drawing" width="800"/>

- Figure 14:
<img src="./figs/merge/fig14.png" alt="drawing" width="800"/>

#### 1.3. Regression Discontinuity Design 

*Tables refer to the paper* 


HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig5](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig5)
<img src="./figs/merge/fig5.png" alt="drawing" width="800"/>
#### Figure 6: 
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig6](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig6)
<img src="./figs/merge/fig6.png" alt="drawing" width="800"/>
#### Figure 7: 
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig7](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig7)
<img src="./figs/merge/fig7.png" alt="drawing" width="800"/>
#### Figure 8: 
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig8](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig8)
<img src="./figs/merge/fig8.png" alt="drawing" width="800"/>
#### Figure 9: 
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig9](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig9)
<img src="./figs/merge/fig9.png" alt="drawing" width="800"/>

####  Figure 10:
<img src="./figs/merge/fig10.png" alt="drawing" width="800"/>

####  Figure 11:
<img src="./figs/merge/fig11.png" alt="drawing" width="800"/>


####  Figure 15:
<img src="./figs/merge/fig15.png" alt="drawing" width="800"/>

####  Figure 16:
<img src="./figs/merge/fig16.png" alt="drawing" width="800"/>

####  Figure 17:
<img src="./figs/merge/fig17.png" alt="drawing" width="800"/>

####  Figure 18:
<img src="./figs/merge/fig18.png" alt="drawing" width="800"/>

## NFT

#### Figure 19:
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN1](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN1)
<img src="./figs/NFT/figN1.png" alt="drawing" width="800"/>

#### Figure 20:
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN2](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN2)
<img src="./figs/NFT/figN2.png" alt="drawing" width="800"/>

#### Figure 21:
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN3](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN3)
<img src="./figs/NFT/figN3.png" alt="drawing" width="800"/>

#### Figure 22:
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN4](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN4)
<img src="./figs/NFT/figN4.png" alt="drawing" width="800"/>

#### Figure 23:
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN5](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN5)
<img src="./figs/NFT/figN5.png" alt="drawing" width="800"/>

#### Figure 24:
HTML: [https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN6](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN6)
<img src="./figs/NFT/figN6.png" alt="drawing" width="800"/>

#### Figure 25:
<img src="./figs/NFT/figP1.png" alt="drawing" width="800"/>

#### Figure 26:
<img src="./figs/NFT/figP2.png" alt="drawing" width="800"/>

#### Figure 27:
<img src="./figs/NFT/figP3.png" alt="drawing" width="800"/>

#### Figure 28
<img src="./figs/NFT/figP4.png" alt="drawing" width="800"/>

#### Figure 29
<img src="./figs/NFT/figP5.png" alt="drawing" width="800"/>


#### Figure 30
<img src="./figs/NFT/figP6.png" alt="drawing" width="800"/>

#### Figure 31
<img src="./figs/NFT/figP7.png" alt="drawing" width="800"/>

#### Figure 32
<img src="./figs/NFT/figP8.png" alt="drawing" width="800"/>

