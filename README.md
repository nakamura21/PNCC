# PNCC implementation in Python
Based on 
- http://www.cs.cmu.edu/~robust/Papers/OnlinePNCC_V25.pdf
- https://www.eurasip.org/Proceedings/Eusipco/Eusipco2015/papers/1570104069.pdf

put a slide about PNCC
- https://www.slideshare.net/ssuser3f97dd/dl-hucks-pncc

## Installation:
Clone and install requirements.
```bash
cd ~
git clone https://github.com/supikiti/PNCC.git
cd PNCC
pip install -r requirements.txt
```

```bash
$ python train.py --lstm-node 32 --recurrent-dropout 0.5 --epochs 10 --optimizer-method adam
```
```bash
$ python train.py -l 32 -r 0.5 -e 10 -r adam
```
```bash
$ pip install keras 
```
```bash
$ pip install librosa 
```
```bash
$ pip install soundfile
```

```bash
$ python predict.py sample.wav
```

`csj_parser.py`のオプションは以下の通りです。

引数 | 説明
-------------|------------
--lstm-node, -l | LSTMのノード数(デフォルト32)
--recurrent-dropout, -d | 再帰の線形変換においてdropするユニットの割合(デフォルト0.5)
--epochs, -e | モデルを訓練するエポック数(デフォルト10)
--optimizer-method, -r | 用いる最適化アルゴリズム(デフォルトadam)
--voice-data, -f | 訓練用データ(trainデータ)と検証データ(testデータ)が存在するディレクトリへのパス(デフォルト./corpus/)


## Licence

[MIT](https://github.com/tcnksm/tool/blob/master/LICENCE)

## Author

[supikiti](https://github.com/supikiti)
