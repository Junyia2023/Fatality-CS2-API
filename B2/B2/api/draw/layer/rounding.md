## rounding

此枚举用于确定圆角形状的圆角处理方式。

## tl

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

圆化左上角。

## tr

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

圆化右上角。

## bl

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

圆化左下角。

## br

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

圆化右下角。

## t

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

圆化两个顶部角。这与使用 `bit.bor(draw.rounding.tl, draw.rounding.tr)` 产生相同的结果。

## l

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

圆化两个左侧角。这与使用 `bit.bor(draw.rounding.tl, draw.rounding.bl)` 产生相同的结果。

## r

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

圆化两个右侧角。这与使用 `bit.bor(draw.rounding.tr, draw.rounding.br)` 产生相同的结果。

## b

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

圆化两个底部角。这与使用 `bit.bor(draw.rounding.bl, draw.rounding.br)` 产生相同的结果。

## all

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

圆化所有角。这与使用 `bit.bor(draw.rounding.tl, draw.rounding.tr, draw.rounding.bl, draw.rounding.br)` 产生相同的结果。