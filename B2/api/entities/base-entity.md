## base_entity

此类型表示基础游戏实体。

> 此类型可能会返回任何其他抽象实体类，但内部将指向正确的类型。

## __index

[![函数][此字段是一个函数，必须使用点 (.) 调用]rw]

尝试在此类中搜索字段。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| `name` | `string` | 字段名称。 |

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| [`schema_accessor_t`](/api/entities/base-entity/schema-accessor-t "此类型表示引用实体对象中某个字段的特殊结构。") | 访问器实例。 |

**示例**

```