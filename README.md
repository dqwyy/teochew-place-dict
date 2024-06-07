# Teochew Place Dict

## 简介
本仓库是为中州韵输入法引擎（Rime/小狼毫/鼠鬚管）设计的潮汕地区行政区划地名词库，词库中不包含拼音编码，故通用于所有音码输入方案。词库中的词条包含潮汕地区及其周边文化辐射地区的乡级（镇/街道）和村级（村/社区）行政区划，数据来源于[modood/Administrative-divisions-of-China](https://github.com/modood/Administrative-divisions-of-China)和[国家统计局- 统计用区划代码和城乡划分代码](https://www.stats.gov.cn/sj/tjbz/tjyqhdmhcxhfdm/2023/index.html)，故不包括更为详细的交通道路名称、建筑物名称、商铺名称、没有村委会的自然村等。如需这些详细的地名作为词库，可参考[搜狗细胞词库](https://pinyin.sogou.com/dict/cate/index/198)、[百度输入法词库](https://shurufa.baidu.com/dict_list?cid=171)、[QQ输入法词库平台](https://cdict.qq.pinyin.cn/v1/list?sort1=%E5%9F%8E%E5%B8%82%E5%9C%B0%E5%8C%BA&sort2=%E5%B9%BF%E4%B8%9C)等输入法提供的词库，这些词库主要通过地图软件抓取，但词条可能因长久未更新而过时。

## 使用
根目录下的`teo_place.dict.yaml`即为词库文件，适用于中州韵输入法，如果你使用其他的输入法，也可以通过[深蓝词库转换](https://github.com/studyzy/imewlconverter)这一工具自行转化为对应的输入法词库格式，支持搜狗、百度、QQ、微软等输入法。

将词库文件复制到中州韵输入法的用户目录或程序目录，在原有方案使用的词库文件中的配置区引入本词库：
```yaml
import_tables:
  - teo_place
```

## 子集
一般情况下，使用上述提及的词库文件即可满足需求。如果有子集需求，例如为了避免重码过多或为了提高部署速度而仅需要其中某个地级市的词条，可参考`subset/`子集文件夹中的词条文件，该文件夹中的词条文件是纯文本格式，使用前需自行转化至符合输入法的词库格式要求。各文件名含义如下：
- `cz.txt`：潮州市行政区划词库，不带后缀，适用于日常交流等大多数场景，推荐使用。
- `cz_suffix.txt`：潮州市行政区划词库，带「镇、街道、村、社区」等区划名称后缀，仅适用于填写信息表格等少量场景，不推荐单独使用，建议与上方的无后缀版合并后使用。
- `st.txt`：汕头市行政区划词库，不带后缀
- `st_suffix.txt`：汕头市行政区划词库，带后缀
- `jy.txt`：揭阳市行政区划词库，不带后缀
- `jy_suffix.txt`：揭阳市行政区划词库，带后缀
- `sw.txt`：汕尾市行政区划词库，仅包含陆丰市三甲地区，不带后缀
- `sw_suffix.txt`：汕尾市行政区划词库，仅包含陆丰市三甲地区，带后缀
- `mz.txt`：梅州市行政区划词库，仅包含丰顺县𨻧隍镇、汤南镇、汤坑镇、黄金镇，不带后缀
- `mz_suffix.txt`：梅州市行政区划词库，仅包含丰顺县𨻧隍镇、汤南镇、汤坑镇、黄金镇，带后缀

## 联络 / Contact
有任何问题欢迎通过Email联络 me@dqwyy.moe

本仓库通过[CC0协议](https://creativecommons.org/publicdomain/zero/1.0/)释出至公有领域，欢迎将此词库转载到其他平台或上传到各输入法的词库平台，无需署名。