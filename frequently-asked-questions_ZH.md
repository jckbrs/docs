---
简介: 常见问题
---

# 常见问题

**为什么使用tendermint的拜占庭容错算法（BFT）？**  
Tendermint的算法是经典的BFT算法，三分之二的验证者需要同意。这个算法可以保证跨链网络的安全性同时对共识有一锤定音的能力。
  
**为什么要用鲁恩币（RUNE）来作为每个资金池的结算单位？**  
如果每个资金池都有两个货币组成，比如BTC:ETH，那么就有拓展能力的问题，因为总共有N*(N-1)/2种不同的方法来配对两种货币。当使用鲁恩币来结算时，不仅可以很容易的交换任意两个货币，同时让网络能对资产的价值有正确的评估。
  
**为什么使用单向碟（1-way state peg) 而不是双向碟或者原子交换呢？**  
总体来说，跨链技术是优于原子交换的。原子交换有较为复杂的签名程序，并且需要甲方乙方的互动。跨链技术加上连续的资金池去除了甲方乙方的必要性，并且资产的交换可以更快的进行（一秒以内）。
单向碟优于双向碟是因为单向碟不需要使用包装过的资产（wrapped token:Wbtc），你可以直接使用原始的资产（BTC）。

**会有稳定币的资金池吗？**  
我们将会创建一个USDr资金池，这个资金池将会连接到不同的稳定币，减少使用单一稳定币的风险同时让套利者将USDr的价格维持1USD。 USDr将使用债务凭证（collateralised debt positions）来保证流动性和安全性。

**质押货币有封锁时间吗？**  
质押的时间和数量都没有限制，想来就来，想走就走。   
  
**货币政策是怎么样的？**  
我们的目标是有一个固定的供应量。
相对以太坊的无限供应或者比特币的趋向零的有限供应，团队希望有序的产出货币（权衡流动供应和总供应+销毁费用）。
五百亿的货币会渐渐的产出给节点，保障安全和资金流动性。

**团队的主要目标是盈利吗？**  
否，网络产生的手续费全部会返还给网络的使用者。整个网络没有针对团队的盈利模式，赚取的费用会全部给质押者，鲁恩币的产出直接给节点操作者。团队唯一的获利模式就是和大家一样持有鲁恩币。
  
**预估的质押收益率？**  
风险高的资金池（市值低的币）：年化百分之十以上 <br />
风险低的资金池（市值高的币:BTC,BNB）：年化百分之三到八

**Asgard钱包是团队建立还是第三方？** <br />
钱包由团队打造， 代码在此 [GitLab](https://gitlab.com/thorchain/asgard-wallet).

**雷神链是怎么判断币价的？需要用外在的信息吗（oracle, weighted average）？** <br />
雷神链不需要和外界沟通来知晓币价，币价由连续资金池和套利交易者来制定。当池的资金不平衡时，套利机器人将会试图平衡资金池。雷神链知道币价的原因是鲁恩币是所有池的结算货币。详情：[Prices](how-it-works/prices.md).