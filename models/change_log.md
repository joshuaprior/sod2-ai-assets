# Base Screen Model
The base screen models role is to determine which item on the
base menu currently has selection focus. The model is designed
to detect the focus by determining what tooltip exists and which
item it is pointing to. Then the model will capture the icon
from that item to determine which item it is.

## Model v0.1.0
This version of the model is able to detect which of six facility
slots has the selection focus.

### Training
The model was trained using in-memory training techniques. It
trained in two phases: FC, and fine tuning. The FC run had
twenty epochs with each epoch generating one thousand unique
images per class. The fine tuning run had just two epochs with only
one hundred unique images generated per class.

### FC training characteristics
Epochs: 20\
Images per class: 1000

|Epoch |Loss |
|------|-----|
| 1|2.8266|
| 2|2.5437|
| 3|2.2656|
| 4|2.1510|
| 5|1.9174|
| 6|1.8854|
| 7|1.9771|
| 8|1.6989|
| 9|2.0276|
|10|1.7064|
|11|1.7400|
|12|1.6128|
|13|1.6052|
|14|1.5194|
|15|1.2952|
|16|1.5082|
|17|1.5510|
|18|1.2250|
|19|1.5821|
|20|1.4351|

### Fine tuning training characteristics
Epochs: 2\
Images per class: 100

|Epoch|Loss|
|-----|----|
|1|0.0088|
|2|0.0021|