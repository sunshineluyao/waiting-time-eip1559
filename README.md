# Understand Waiting Time in EIP-1559 Transaction Fee Mechanisms

## Project information
- **Authors**: 
- **Acknowledgments**: This research is supported as an independent project supported by Ethereum Academic Grants Round.
- **Project Summary**: 
Blockchain enables peer-to-peer transactions in cyberspace without a trusted third party. The rapid growth of Ethereum and smart contract blockchains in general — calls for well-designed Transaction Fee Mechanisms (TFMs) to allocate limited storage and computation resources. However, existing research on TFMs needs to consider the waiting time of transactions, which is essential for both computer security and economic efficiency, though often mentioned in different words, such as latency or market congestion. Integrating data from the Ethereum blockchain and mempool, we explore how two types of shocks affect transaction latency. First, we apply regression discontinuity design (RDD) to study the causal inference of the Merge, the most recent significant upgrade of Ethereum. Our results show that the Merge significantly reduces the long waiting time and market congestion. Then, we apply time series analysis to research the interaction of significant NFT drops and market congestion using Facebook Prophet, an open-source algorithm for generating time-series models. Our analysis reveals that the models could significantly improve the forecast of market congestion by considering NFT drops as a shock. Our study contributes to the interdisciplinary research at the intersection of computer security, distributed systems, market design, causal inferences, and time series analysis. Our findings shed light on a new direction of TFMs that prevent market congestion by efficiently forecasting ex-ante other than the current ex-post treatments. 

## Table of Contents
- [data](https://github.com/sunshineluyao/waiting-time-eip1559/tree/main/data)
- [code](https://github.com/sunshineluyao/waiting-time-eip1559/tree/main/code)
- [figs](https://github.com/sunshineluyao/waiting-time-eip1559/tree/main/figs)


## data
```
data
├── processed_data
│   ├── merge_sanctioned.csv
│   ├── sanctioned_after.md
│   ├── sanctioned_before.md
│   ├── sanctioned_transaction_from.csv
│   └── sanctioned_transaction_to.csv
└── queried_data
    └── sanction.csv
```

### The Merge Data Range
- the total number of blocks=140,000
- the total number of transactions= 23,871,253

|type            | from                | to                  |
|----------------|---------------------|---------------------|
| date_time      | 2022-09-03 20:10:39 |2022-09-25 02:27:11  |
| unix_timestamp |1662235839.0	       |1664072831.0         |
| block number   |15467393	           |15607393             |


### The NFT Data Range
- the total number of blocks = 181,075
|type              | from                 | to                |
|-----------------|-----------------------|-------------------|
| date_time       |2021-08-04 00:00:00    |2021-09-21 00:00:00|
| unix_timestamp  |1629763200.0           |1632182400.0       |
| block number    |13084679               |13265754           |



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

```
figs
├── Result 1: the merge
│   ├── 1.1. The waiting time (delay)
│   │   ├── 1.1.1. Visualization
│   │   ├── 1.1.2. Moving Average Smoothing
│   │   └── 1.1.3. Regression Discontinuity
│   ├── 1.2. The market congestion (efficiency)
│   │   ├── 1.2.1. Visualization
│   │   ├── 1.2.2. Moving Average Smoothing
│   │   └── 1.2.3. Regression Discontinuity
│   └── 1.3. The gas used per second (security)
│       ├── 1.2.1. Visualization
│       ├── 1.2.2. Moving Average Smoothing
│       └── 1.2.3. Regression Discontinuity
├── Result 2: The NFT drops
│   ├── 2.1. Visualization
│   └── 2.2. The Time Series Forecast
└── Result 3: The Confounding Factors
    ├── 3.1. The Network for Sanctioned Transactions
    ├── 3.2. Sanctioned Transactions with Unobserved Delay (Only found after the merge)
    └── 3.3. Relevance Statistics for the Delay
        ├── 3.3.1. observed and unobserved delay before and after the merge
        ├── 3.3.2. sanctioned and unsanctioned transactions before and after the merge
        └── 3.3.3. statistics for the delay of the sanctioned and unsanctioned transactions before and after the merge
```

### Result 1: the merge

#### 1.1. The Waiting Time (delay)

##### 1.1.1. Visualizations
- Figure 1

[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig1)
<img src="./figs/merge/fig1.png" alt="drawing" width="800"/>
- Figure 2: 

[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig2)
<img src="./figs/merge/fig2.png" alt="drawing" width="800"/>

- Figure 3: 

[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig3)
<img src="./figs/merge/fig3.png" alt="drawing" width="800"/>
- Figure 4: 

[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig4)
<img src="./figs/merge/fig4.png" alt="drawing" width="800"/>

##### 1.1.2. Moving Average Smoothing

- Figure 12:

<img src="./figs/merge/fig12.png" alt="drawing" width="800"/>


- Figure 13:
<img src="./figs/merge/fig13.png" alt="drawing" width="800"/>

- Figure 14:
<img src="./figs/merge/fig14.png" alt="drawing" width="800"/>


- Figure 16:
<img src="./figs/merge/fig16.png" alt="drawing" width="800"/>

##### 1.1.3. Regression Discontinuity Design 

*Tables refer to the paper* 



#### 1.2. The Market Congestion
##### 1.2.1. Visualization
- Figure 10:
<img src="./figs/merge/fig10.png" alt="drawing" width="800"/>

- Figure 11:
<img src="./figs/merge/fig11.png" alt="drawing" width="800"/>

##### 1.2.2. Moving Aveage Smoothing

- Figure 17:
<img src="./figs/merge/fig17.png" alt="drawing" width="800"/>

- Figure 18:
<img src="./figs/merge/fig18.png" alt="drawing" width="800"/>

##### 1.2.3. Regression Discontinuity Design 

*Tables refer to the paper* 


#### 1.3. The Gas Used Per Second

##### 1.3.1. Visualization

- Figure 19
<img src="./figs/merge/figLoad1.png" alt="drawing" width="800"/>

- Figure 20
<img src="./figs/merge/figLoad2.png" alt="drawing" width="800"/>


##### 1.3.2. Moving Aveage Smoothing

- Figure 21
<img src="./figs/merge/figLoad3.png" alt="drawing" width="800"/>

##### 1.3.3. Regression Discontinuity Design 
*Tables refer to the paper*

## Results 2: NFT Drops

### 2.1.Visualization

#### Figure 19:
[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN1)
<img src="./figs/NFT/figN1.png" alt="drawing" width="800"/>

#### Figure 20:
[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN2)
<img src="./figs/NFT/figN2.png" alt="drawing" width="800"/>

#### Figure 21:
[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN3)
<img src="./figs/NFT/figN3.png" alt="drawing" width="800"/>

#### Figure 22:
[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN4)
<img src="./figs/NFT/figN4.png" alt="drawing" width="800"/>

#### Figure 23:
[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN5)
<img src="./figs/NFT/figN5.png" alt="drawing" width="800"/>

#### Figure 24:
[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/NFT/figN6)
<img src="./figs/NFT/figN6.png" alt="drawing" width="800"/>


### 2.2. The Time Series Forecast

#### The congestion ratio

#### Figure 25:
<img src="./figs/NFT/figP1.png" alt="drawing" width="800"/>

#### Figure 26:
<img src="./figs/NFT/figP2.png" alt="drawing" width="800"/>

#### Figure 27:
<img src="./figs/NFT/figP3.png" alt="drawing" width="800"/>

#### Figure 28
<img src="./figs/NFT/figP4.png" alt="drawing" width="800"/>

#### The continued congestion ratio

#### Figure 29
<img src="./figs/NFT/figP5.png" alt="drawing" width="800"/>

#### Figure 30
<img src="./figs/NFT/figP6.png" alt="drawing" width="800"/>

#### Figure 31
<img src="./figs/NFT/figP7.png" alt="drawing" width="800"/>

#### Figure 32
<img src="./figs/NFT/figP8.png" alt="drawing" width="800"/>



### Result 3: the Comfounding Factors

####3.1. The Network for Sanctioned Transactions

##### Figure 33
<img src="./figs/Sanction/sanctioned.png" alt="drawing" width="800"/>

##### Figure 34
<img src="./figs/Sanction/sanctioned_before.png" alt="drawing" width="800"/>

##### Figure 35
<img src="./figs/Sanction/sanctioned_after.png" alt="drawing" width="800"/>

#### 3.2 Sanctioned Tranctions with Unobserved Delay (Only After the Merge)
| OFAC Sanctioned address Interacted          | hash                                                               |
|:-------------------------------------------|:-------------------------------------------------------------------|
| 0xd90e2f925da726b50c4ed8d0fb90ad053324f31b | 0x0fb9a4e23d7c504571daed1394feea8bcb823a18a2887e7cab54f7fa4ffa2981 |
| 0xd90e2f925da726b50c4ed8d0fb90ad053324f31b | 0xb37f8b00993271dd97ac9acdb4d84cb31cd210a037286bcc4bc7887f0008a81f |
| 0xd90e2f925da726b50c4ed8d0fb90ad053324f31b | 0xd5c80d358016a1fe77260fa9cab88a706337c6f41f9112eca8840e9233794e82 |
| 0xd90e2f925da726b50c4ed8d0fb90ad053324f31b | 0x52cd1910b0710e73a9fb85f9e13861ef828a3244a1fa03944e47adf38ac9f851 |
| 0xd90e2f925da726b50c4ed8d0fb90ad053324f31b | 0xe4a84c77748a627a093f79c6abb4b037c60ae9f58977bab2c46d17a657f2afcd |
| 0xd90e2f925da726b50c4ed8d0fb90ad053324f31b | 0x094cd7a9dc72cf6b3415fd18223a075e631d4ee5bfc900b9293dbd135db24334 |
| 0xd90e2f925da726b50c4ed8d0fb90ad053324f31b | 0x78c426d5b25290aa03153c728383f2d422c7a14a40a0a5e11bea67c104e5e295 |
| 0xd90e2f925da726b50c4ed8d0fb90ad053324f31b | 0x9d4fcf6315d8fbf2e07dc71a2c81df8c86a2dd518ac76c48eaeb397e28e95ca8 |
| 0xd90e2f925da726b50c4ed8d0fb90ad053324f31b | 0x0b9613f988da92901816bc76af743974032985b5eeeab70d5940c65b9f7faca6 |

#### 3.3. Relavant Statistics for the Delay

##### 3.3.1. observed and unobserved delay before and after the merge

|   merge |  delay observed | delay unobserved |
|--------:|------------:|-------:|
|before the merge | 1.19478e+07 | 326561 |
|after the merge| 1.10589e+07 | 537997 |

##### 3.3.2. sanctioned and unsanctioned transactions before and after the merge

|   sanctioned|      before  the merge |            after  the merge|
|-------------:|---------------:|--------------:|
|            no |    9.71282e+06 |   9.12023e+06 |
|            yes | 1007           | 466           |

##### 3.3.3. statistics for the delay for sanctioned and unsanctioned transactions before and after the merge

|        |          count |     mean |        std |      min |      25% |     50% |     75% |            max |
|:-------|---------------:|---------:|-----------:|---------:|---------:|--------:|--------:|---------------:|
| (non-sanctioned, before) |    9.71282e+06 |  974.101 |  37825.7   | 2e-05    |  7.794   | 15.1918 | 29.6824 |    5.44163e+06 |
| (non-sanctioned, after) |    9.12023e+06 | 4868.07  | 152958     | 6.4e-05  |  9.14709 | 13.7926 | 18.6293 |    6.29244e+06 |
| (sanctioned, before) | 1007           | 6161.2   | 131471     | 0.115805 | 10.0729  | 19.6879 | 37.1808 |    2.95086e+06 |
| (sanctioned, after) |  466           |   47.262 |    257.401 | 1.03641  | 11.8761  | 17.1533 | 22.5716 | 3107.16        |

### Appendix

#### The Transaction Count

- Figure 9: 
[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig9)
<img src="./figs/merge/fig9.png" alt="drawing" width="800"/>

#### The Gas Used Percentage

#####  Visualization
- Figure 5

[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig5)

<img src="./figs/merge/fig5.png" alt="drawing" width="800"/>

- Figure 6: 

[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig6)
<img src="./figs/merge/fig6.png" alt="drawing" width="800"/>

- Figure 7: 

[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig7)
<img src="./figs/merge/fig7.png" alt="drawing" width="800"/>

##### Moving Aveage Smoothing
- Figure 8: 

[Click here to see the interactive figure](https://sunshineluyao.github.io/waiting-time-eip1559/figs/merge/fig8)
<img src="./figs/merge/fig8.png" alt="drawing" width="800"/>

- Figure 15:
<img src="./figs/merge/fig15.png" alt="drawing" width="800"/>

##### Regression Discontinuity Design 

*Tables refer to the paper* 


