### Reverse Engineering in Dispersion Engineering

Prediction of simulation parameters.

#### Downloading REDE dataset

```python
from utils.dataset import REDE
import torchvision.transforms as transforms

train_dataset = REDE('data/rede', train=True, download=True,
                     transform=torchvision.transforms.ToTensor())
test_dataset = REDE('data/rede', train=False, download=True,
                     transform=torchvision.transforms.ToTensor(),
                     test_indices=train_dataset.test_indices)
```

#### Image samples from dataset

<img src='img/img1.jpg' width=600>

And corresponding parameters of simulated models: (gap, width1, height, radius1, width2).
```
1.00000e-05 *
  0.0250  0.1550  0.0850  2.2000  0.0880
  0.0300  0.1450  0.0700  2.0000  0.0920
  0.0250  0.1550  0.0700  2.2000  0.0920
  0.0350  0.1500  0.0750  2.0000  0.1000
[torch.FloatTensor of size 4x5]
```

See [[main.ipynb](main.ipynb)] for more information.

#### Preprocessing of raw data

<img src='img/img2.jpg' width=600>

To get processed values you can visit [[dispersion_values.ipynb](utils/dispersion_values.ipynb)].

#### Contributors
* Anton Lukashchuk &lt;[anton.lukashchuk@epfl.ch](mailto:anton.lukashchuk@epfl.ch)&gt;
* Anton Karazeev &lt;[anton.karazeev@phystech.edu](mailto:anton.karazeev@phystech.edu)&gt;
