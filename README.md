# gubo
对于电信用户来说，国外的VPS的选择是简单而痛苦的，因为除了CN2线路接入的机房，其它线路接入的VPS都会出现丢包率高，绕道等情况的出现，导致VPS访问速度慢，甚至近乎于不可用的状态。接下来就给大家简单介绍一下CN2线路，选购注意事项及一些CN2接入的VPS提供商。

CN2线路介绍
CN2全称为中国电信下一代承载网，英文Chinatelecom Next Generation Carrier Network，缩写为CNCN(扯蛋的缩写)，进一步缩写为CN2(扯蛋的进一步缩写)。

为什么CN2速度那么快
CN2作为“精品网络项目”被提出来，其技术构造是远远领先于电信原有网络的，极为先进的QOS保证网络的畅通性，具体可参考资料。当然除了先进的技术，其昂贵的价格和对大量网络资源的独占性也是重要的原因，资料。普通家庭宽带用户用不上CN2线路，哪怕加几倍的钱也不一定能用上，而接入CN2线路机房的VPS，价格卖得比其他线路的高很多。用户少，服务器少，分配的独享资源多，这样就能保证绝大多数情况下CN2线路的流畅性。

如果想要寻找接入CN2线路的国外VPS提供商，建议使用“Next Carrier Network”这个关键词，但是其实只要有CN2接入的机房，都会被广为流传，国内分销商涌入，所以大家想要选购，找国人商家提供的产品会好找得多。

CN2 GIA和 CN2 GT
之前关于CN2里双向/单向，全程/半程的说法并不严谨。关于CN2的等级划分中国电信有自己官方的名称。我们需要关注的有163骨干网，CN2 GT和CN2 GIA。

普通163: 就是电信用户最经常遇到的电信线路，等级最低，省级/出国/国际骨干节点都以202.97开头，全程没有59.43开头的CN2节点。在出国线路上表现为拥堵，丢包率高。
CN2 GT: CN2里属于Global Transit的产品(又名GIS-Global Internet Service)，在CN2里等级低，省级/出国节点为202.97开头，国际骨干节点有2～4个59.43开头的CN2节点。在出国线路上拥堵程度一般，相对于163骨干网的稍强。
CN2 GIA: CN2里属于Global Internet Access的产品，等级最高, 在部署有CN2节点的省份就近接入该省的省级CN2节点(参考ipip陕西宝鸡电信节点)，在没部署CN2节点的省份则就近接入部署有CN2节点的省份的CN2节点(参考ipip内蒙古呼和浩特电信节点，在北京接入CN2路由），GIA CN2不保证全程没有202.97节点，而是“就近”接入CN2（参考ipip江苏镇江电信节点，经南京202.97节点进入江苏南京CN2节点)，丢包率总体较低。在出国线路上表现最好，很少拥堵，理论上速度最快最稳定
关于更多更详细的资料，请查看此文章: 普及下电信直连、CN2（GIA）、本土运营商
注意：以上关于速度方面的描述都是理论，实际影响速度的重要因素还有拥堵程度。QuadraNET的某几个服务商虽然用的是普通163线路，但总体表现一直不错，有时候甚至比某些拥堵不堪的CN2 GT商家比如BudgetVM还更好。


CN2线路的陷阱
CN2线路本身的优越性是无需置疑的，但是，影响VPS速度的因素绝不只有接入线路本身，商家的服务水平也至关重要。随着国内出国线路（尤其是电信）的愈发拥堵，优质线路需求愈发强烈，商家要面对的压力会更大。但凡连接速度稍微快一点的VPS产品，如果没有合理的技术手段，客户里的SS销售商基本都能将带宽跑满，各种加倍发包软件让同服务器的其它客户跑不上速度。下面给大家总结一下需要注意的地方：

 便宜CN2需谨慎 ：很简单，便宜的CN2谁都想要，而且用来卖SS利润高。于是是个人都买，都用来开设代理卖给其他人，由于成本低，就算滥用被处罚的损失也小。最典型的案例就是BudgetVM，几乎在2016年3月19日开放介入CN2线路当天就已经拥堵到瘫痪，坚持没几个月就不得不取消CN2线路的接入，即使这样，到今天速度也还没恢复到正常水平(参考链接)。某种程度来说，高价格是高速度的保证。另外最好的例证就是Softlayer香港（非CN2），当初超大流量+超低价格引得无数人争相购买，现在已经沦落到绕道美国再回国内(参考链接)。CN2就是依靠其定价高才能保持流畅性，低价大量销售的结果必然是挤爆，速度得不到保证。
 单向CN2需谨慎 ：单向CN一般都是去程CN2，回程普通电信线路。最为典型的是Hostus家，无数Hostus推介网站竞相宣布Hostus的LA KVM构架VPS接入CN2，我也被忽悠入手了一个，一开始以为路由还没优化完毕速度慢，后来官方客服澄清只有国内使用CN2精品网业务的才会走CN2线路，我用精品网业务了还要你这作甚？！原话：”We have both China Telecom and CN2 now in LAX02. Your ISP will, by default, prefer China Telecom AS4134 routes unless you have an active CN2 subscription within China.”
目前来说，香港CN2线路70～90元一个月，带宽峰值2M～3M或者流量400G/月属于正常范围，低于这个价格长期大量有货的请慎重！.
