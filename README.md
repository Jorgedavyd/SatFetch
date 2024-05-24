![status](https://img.shields.io/badge/status-beta-red.svg)
[![license](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![code-style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![pypi]]
# StarStream

<p align="center">
  <img src="https://raw.githubusercontent.com/Jorgedavyd/starstream/main/docs/source/logo.png"/>
</p>

Asynchronous satellite data downloading for CDAWeb, JSOC, etc.

## Spacecrafts and datasets
<img src="https://upload.wikimedia.org/wikipedia/commons/9/9b/ACE_mission_logo.png" height=200 width=200> <img src="https://www.nesdis.noaa.gov/s3/styles/webp/s3/migrated/DSCOVR-Logo_NOAA_NASA_USAF.png.webp?itok=EGpby_uX" height=200 width=350>
<img src="https://wdc.kugi.kyoto-u.ac.jp/figs/logoh.gif" height=200 width=300><img src="https://upload.wikimedia.org/wikipedia/commons/d/d0/Windlogo.gif" height=200 width=200>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/85/Jaxa_logo.svg/1024px-Jaxa_logo.svg.png" height=150 width=300> <img src='https://upload.wikimedia.org/wikipedia/commons/thumb/e/e5/NASA_logo.svg/1224px-NASA_logo.svg.png' height = 200 width = 250>
<img src="https://3.bp.blogspot.com/-YdNujMhGAkI/WeIyjnfiN8I/AAAAAAABAII/JDV2MvutF_kNJ9ManBMmTM-0X4G6m3KiACLcBGAs/s1600/logo_sdo.gif" height = 200 width = 200> <img src="https://lh3.googleusercontent.com/proxy/CuvQ0w53zAeiZ3s1NT1ijGN6Lz801QNO6toQw2ZzwE-3_FTi7bZkin0Q0mzhisLX0Q1_0ftGyYvR4HIxstI5TIJ9rrp6KfFUz47jWfZD" height = 200 width = 200>
<img src="https://earth.esa.int/eogateway/documents/20142/0/swarm.png/656b6a23-f035-f7e3-78c6-02a47d1a4b6e?t=1608141199732" height = 100 width = 300><img src="http://esdcdoi.esac.esa.int/doi/html/img/Proba2_logo2020.svg" height = 200 width = 200>

## Example
```python 
from starstream import ACE, DSCOVR
from starstream.utils import DataDownloading
from datetime import datetime
import asyncio

async def main():
    await DataDownloading(
        [
            ACE(),
            DSCOVR()
        ],
            (datetime(2014, 12, 12), datetime(2014, 12, 30))
    )

if __name__ == '__main__':
    asyncio.run(main())
    
```
## Citation

```
@misc{starstream,
  author = {Jorge Enciso},
  title = {StarStream: An Open-Source Asynchronous Data Downloader},
  howpublished = {\url{https://github.com/Jorgedavyd/starstream}},
  year = {2024}
}
```