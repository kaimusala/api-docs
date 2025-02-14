[Util](Util.Util.md) / LocaleUtil

# LocaleUtil <Badge type="tip" text="Namespace" /> <Score text="LocaleUtil" />

## Table of contents

| Functions |
| :-----|
| **[getDefaultLocale](Util.LocaleUtil.md#getdefaultlocale)**(): `string` <br> 获取默认的语言和地区|

## Functions

### getDefaultLocale <Score text="getDefaultLocale" /> 

• **getDefaultLocale**(): `string` 

获取默认的语言和地区


使用示例:调用方法
```ts
const locale = LocaleUtil.getDefaultLocale();
console.log(`locale: ${locale}`);
// zh-CN
```

#### Returns

`string`

以IETF语言标签表示的字符串包含:ISO 639-1 两位字母语言码 (如, "zh");
可选ISO 15924 四位字母脚本码 (如, "Hans");
可选ISO 3166-1 国家码 (如, "CN")
