# learning_content

## template
```json
{
    "update_time": "2023-08-01 03:25:14",
    "author": "Luna Gao",
    "email": "gao.xue.qi1@gmail.com",
    "support_version": ">=1.0.0 <2.0.0",
    "version": 1,
    "uuid": "8c8ad22c-345a-4dcb-b751-0f2adf801197", // 可由此生成： https://1024tools.com/uuid
    "image": [
        {
            "key": "en",
            "value": "https://remember-hub.oss-cn-beijing.aliyuncs.com/English/white.png"
        },
        {
            "key": "zh",
            "value": "https://remember-hub.oss-cn-beijing.aliyuncs.com/English/white.png"
        }
    ],
    "title": [
        {
            "key": "en",
            "value": "English Alphabet"
        },
        {
            "key": "zh",
            "value": "英文字母表"
        }
    ],
    "tag": [
        {
            "key": "en",
            "value": "English"
        },
        {
            "key": "zh",
            "value": "英语"
        }
    ],
    "description": [
        {
            "key": "en",
            "value": "Five of the letters in the English Alphabet are vowels: A, E, I, O, U. The remaining 21 letters are consonants: B, C, D, F, G, H, J, K, L, M, N, P, Q, R, S, T, V, X, Z, and usually W and Y."
        },
        {
            "key": "zh",
            "value": "简介" // 不可为空
        }
    ],
    "value_type": [
        {
            "type": "UpperCase",
            "display_name": [
                {
                    "key": "en",
                    "value": "Upper Case Letters"
                },
                {
                    "key": "zh",
                    "value": "大写字母"
                }
            ]
        },
        {
            "type": "LowerCase",
            "display_name": [
                {
                    "key": "en",
                    "value": "Lower Case Letters"
                },
                {
                    "key": "zh",
                    "value": "小写字母"
                }
            ]
        }
    ],
    "values": [
        {
            "image": null,
            "value": "A",
            "type": "UpperCase"
        },
        {
            "image": null,
            "value": "a",
            "type": "LowerCase"
        }
    ]
}
```

UUID:
https://1024tools.com/uuid


```python
import json

template = {
    "image": None,
    "value": "",
    "type": None
}

words = """天地人你我他
一二三四五上下
口耳目手足站坐
日月水火山石田禾
对云雨风花鸟虫
六七八九十
爸妈马土不画打棋鸡字词语句子桌纸
文数学音乐
妹奶小桥台雪儿白草家是车路灯走
秋气了树叶片大飞会个
的船两头在里看见闪星
江南可采莲鱼东西北
尖说春青蛙夏弯皮冬
男女开关正反
远有色近听无声去还来
多少黄牛只猫边鸭苹果杏桃
书包尺作业本笔刀课早校
明力尘从众双木林森条心
升国旗中红歌起么美丽立
午晚昨今年
影前后黑狗左右它好朋友
比尾巴谁长短把伞兔最公
写诗点要过给当串们以成
彩半空问到方没更绿出长
睡那海真老师吗同什才亮
时候觉得自己很穿衣服门快
蓝又笑向和贝娃挂活金
哥姐弟叔爷
群竹牙用几步为参加洞着
乌鸦处找办旁许法放进高
住孩玩吧发芽爬呀久回全变
工厂医院生""".split()

data = []

for char in words:
    if char != '\n':
        for item in char:
            obj = template.copy()
            obj["value"] = item
            data.append(obj)

json_data = json.dumps(data, ensure_ascii=False)

print(json_data)
```