## 配置环境
本地或服务器部署请配置此环境
```
git clone https://github.com/EXACG/AI-Sound-Web.git
cd /AI-Sound-Web/ && pip install -r requirements.txt
wget -c "https://github.com/LemonFan-maker/Download-Models/releases/download/ys/ys.pth" -P /work/AI-Sound-Web/ys
pip install uvicorn
pip install fastapi
pip install librosa
apt-get update
apt-get -y install libsndfile1
pip install soundflie
pip install unidecode
pip install phonemizer
pip install pypinyin
pip install pypinyin_dict
pip install jieba
pip install Cython
cd /AI-Sound-Web/monotonic_align/ && python setup.py build_ext --inplace
```
Python3.8和Python3.9都可运行 
Python3.10及以上会出现运行库版本不够的情况没法运行

## 食用方法

上面的环境代码配置后,输入```python main.py```

```
http://127.0.0.1:8080/run?speaker=<说话的人>&text=<想说的话> 
```

到时候将``<说话的人>``直接替换为
```
'派蒙', '凯亚', '安柏', '丽莎', '琴', '香菱', '枫原万叶', '迪卢克', '温迪', '可莉', '早柚', '托马', '芭芭拉', '优菈', '云堇', '钟离',
'魈', '凝光', '雷电将军', '北斗', '甘雨', '七七', '刻晴', '神里绫华', '戴因斯雷布', '雷泽', '神里绫人', '罗莎莉亚', '阿贝多', '八重神子',
'宵宫', '荒泷一斗', '九条裟罗', '夜兰', '珊瑚宫心海', '五郎', '散兵', '女士', '达达利亚', '莫娜', '班尼特', '申鹤', '行秋', '烟绯',
'久岐忍', '辛焱', '砂糖', '胡桃', '重云', '菲谢尔', '诺艾尔', '迪奥娜', '鹿野院平藏'
```
以上的任何**一个**即可.

把``<想说的话> ``替换成你想让他说的即可.

比方说
```
http://127.0.0.1:8080/run?speaker=派蒙&text=我要摆烂。 
```
## !!注意!!
文字不要太长，10~20字最好。
