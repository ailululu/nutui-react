# Elevator

### Intro


用于列表快速定位以及索引的显示

### Install

```javascript
import { Elevator } from '@nutui/nutui-react'
```

## Demo

### Basic Usage

:::demo

```tsx
import React from 'react'
import { Elevator } from '@nutui/nutui-react'

const App = () => {
  const dataList = [
    {
      title: 'A',
      list: [
        {
          name: 'AnHui',
          id: 1,
        },
      ],
    },
    {
      title: 'B',
      list: [
        {
          name: 'BeiJing',
          id: 2,
        },
      ],
    },
    {
      title: 'G',
      list: [
        {
          name: 'GuangXi',
          id: 3,
        },
        {
          name: 'GuangDong',
          id: 4,
        },
      ],
    },
    {
      title: 'H',
      list: [
        {
          name: 'HuNan',
          id: 5,
        },
        {
          name: 'HuBei',
          id: 6,
        },
        {
          name: 'Henan',
          id: 7,
        },
      ],
    },
  ]
  const clickItem = (key: string, item: any) => {
    console.log(key, JSON.stringify(item))
  }

  const clickIndex = (key: string) => {
    console.log(key)
  }
  return (
    <Elevator
      indexList={dataList}
      height="260"
      clickItem={(key: string, item: any) => clickItem(key, item)}
      clickIndex={(key: string) => clickIndex(key)}
    />
  )
}
export default App
```

:::

### Custom index

:::demo

```tsx
import React from 'react'
import { Elevator } from '@nutui/nutui-react'

const App = () => {
  const dataList = [
    {
      num: 'One',
      list: [
        {
          name: 'BeiJing',
          id: 1,
        },
        {
          name: 'ShangHai',
          id: 2,
        },
        {
          name: 'ShenZhen',
          id: 3,
        },
        {
          name: 'GuangZhou',
          id: 4,
        },
        {
          name: 'HangZhou',
          id: 5,
        },
      ],
    },
    {
      num: 'Two',
      list: [
        {
          name: 'ChengDu',
          id: 6,
        },
        {
          name: 'XiAn',
          id: 7,
        },
        {
          name: 'TianJin',
          id: 8,
        },
        {
          name: 'WuHan',
          id: 9,
        },
        {
          name: 'ChangSha',
          id: 10,
        },
        {
          name: 'ChongQin',
          id: 11,
        },
        {
          name: 'SuZhou',
          id: 12,
        },
        {
          name: 'NanJing',
          id: 13,
        },
      ],
    },
    {
      num: 'Three',
      list: [
        {
          name: 'XiNing',
          id: 14,
        },
        {
          name: 'LanZhou',
          id: 15,
        },
        {
          name: 'ShiJiaZhuang',
          id: 16,
        },
        {
          name: 'QinHuangDao',
          id: 17,
        },
        {
          name: 'DaLian',
          id: 18,
        },
        {
          name: 'HaErBin',
          id: 19,
        },
        {
          name: 'ChangChun',
          id: 20,
        },
        {
          name: 'TaiYuan',
          id: 21,
        },
      ],
    },
  ]
  const clickItem = (key: string, item: any) => {
    console.log(key, JSON.stringify(item))
  }

  const clickIndex = (key: string) => {
    console.log(key)
  }
  return (
    <Elevator
      indexList={dataList}
      height="220"
      acceptKey="num"
      clickItem={(key: string, item: any) => clickItem(key, item)}
      clickIndex={(key: string) => clickIndex(key)}
    />
  )
}
export default App
```

:::

### Index ceiling

:::demo

```tsx
import React from 'react'
import { Elevator } from '@nutui/nutui-react'

const App = () => {
  const dataList = [
    {
      title: 'A',
      list: [
        {
          name: 'AnHui',
          id: 1,
        },
      ],
    },
    {
      title: 'B',
      list: [
        {
          name: 'BeiJing',
          id: 2,
        },
      ],
    },
    {
      title: 'C',
      list: [
        {
          name: 'ChongQin',
          id: 3,
        },
      ],
    },
    {
      title: 'F',
      list: [
        {
          name: 'FuJian',
          id: 4,
        },
      ],
    },
    {
      title: 'G',
      list: [
        {
          name: 'GuangXi',
          id: 5,
        },
        {
          name: 'GuangDong',
          id: 6,
        },
        {
          name: 'GanSu',
          id: 7,
        },
        {
          name: 'GuiZhou',
          id: 8,
        },
      ],
    },
    {
      title: 'H',
      list: [
        {
          name: 'HuNan',
          id: 9,
        },
        {
          name: 'HuBei',
          id: 10,
        },
        {
          name: 'HaiNan',
          id: 11,
        },
        {
          name: 'HeBei',
          id: 12,
        },
        {
          name: 'HeNan',
          id: 13,
        },
        {
          name: 'HeiLongJiang',
          id: 14,
        },
      ],
    },
    {
      title: 'J',
      list: [
        {
          name: 'JiLin',
          id: 15,
        },
        {
          name: 'JiangSu',
          id: 16,
        },
        {
          name: 'JiangXi',
          id: 17,
        },
      ],
    },
    {
      title: 'L',
      list: [
        {
          name: 'LiaoNing',
          id: 18,
        },
      ],
    },
  ]
  const clickItem = (key: string, item: any) => {
    console.log(key, JSON.stringify(item))
  }

  const clickIndex = (key: string) => {
    console.log(key)
  }
  return (
    <Elevator
      indexList={dataList}
      height="220"
      isSticky
      clickItem={(key: string, item: any) => clickItem(key, item)}
      clickIndex={(key: string) => clickIndex(key)}
    />
  )
}
export default App
```

:::


### Custom Content

:::demo

```tsx
import React from 'react'
import { Elevator, elevatorContext, Icon } from '@nutui/nutui-react'

const App = () => {
  const dataList = [
    {
      title: 'A',
      list: [
        {
          name: 'AnHui',
          id: 1,
        },
      ],
    },
    {
      title: 'B',
      list: [
        {
          name: 'BeiJing',
          id: 2,
        },
      ],
    },
    {
      title: 'G',
      list: [
        {
          name: 'GuangXi',
          id: 3,
        },
        {
          name: 'GuangDong',
          id: 4,
        },
      ],
    },
    {
      title: 'H',
      list: [
        {
          name: 'HuNan',
          id: 5,
        },
        {
          name: 'HuBei',
          id: 6,
        },
        {
          name: 'Henan',
          id: 7,
        },
      ],
    },
  ]
  const clickItem = (key: string, item: any) => {
    console.log(key, JSON.stringify(item))
  }

  const clickIndex = (key: string) => {
    console.log(key)
  }
  return (
    <Elevator
      indexList={dataList}
      height="260"
      clickItem={(key: string, item: any) => clickItem(key, item)}
      clickIndex={(key: string) => clickIndex(key)}
    >
      <elevatorContext.Consumer>
        {(value) => {
          return (
            <>
              <Icon name="JD" size="12" />
              <span style={{ marginLeft: '15px' }}>{value?.name}</span>
            </>
          )
        }}
      </elevatorContext.Consumer>
    </Elevator>
  )
}
export default App
```

:::

## API

### Props

| Attribute                   | Description                                                             | Type    | Default |
|------------------------|----------------------------------------------------------------|---------|------|
| height                 | Height of elevator area                                                    | Number、String  | `200px`
| acceptKey             | Index key value                                                      | String  | `title` |
| indexList             | Index list                                                         | Array（`item` needs to contain `id` and `name` attributes, and `name` supports passing in `html` structure）  | `[{id: 0, name: ''}]` |
| isSticky            | Whether the index is ceiling                                                    | Boolean  | `false` |
| spaceHeight             | Up and down spacing of right anchor point              | Number  | `23` |
| titleHeight             | Height of left index                                                     | Number  | `35` |

### Event

| Event  | Description     | Arguments    |
|-------|----------|-------------|
| click-item | Click content | key: string, item: { id: 0, name: '' } |
| click-index | Click index | key: string |
