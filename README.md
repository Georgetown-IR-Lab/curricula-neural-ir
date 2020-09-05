# Training Curricula for Open Domain Answer Re-Ranking

Sean MacAvaney, Franco Maria Nardini, Raffaele Perego, Nicola Tonellotto, Nazli Goharian, and Ophir
Frieder. *Training Curricula for Open Domain Answer Re-Ranking*. SIGIR 2020.

[PDF](https://arxiv.org/pdf/2004.14269.pdf)

## Code

Code to reproduce the results in the paper is found in [OpenNIR](https://github.com/Georgetown-IR-Lab/OpenNIR).

Relevant configuration:

**Training**

`trainer=pairwise`: Use pairwise training *without* curriculum learning

`trainer=pointwise`: Use pointwise training *without* curriculum learning

`trainer=pairwise_cl`: Use pairwise training with curriculum learning

`trainer=pointwise_cl`: Use pointwise training with curriculum learning

`trainer.curriculum=reciprank`: Use the Reciprocal rank heuristic

`trainer.curriculum=normscore`: Use the Normalized score heuristic

`trainer.curriculum=kdescore`: Use the Kernel Density Estimation (KDE) heuristic

`trainer.eoc_epoch=20`: Sets the End of curriculum iteration ($m$)

**Dataset**

`config/msmarco/judgedtrec2019`: Train and validated on MS-MARCO, test on TREC DL 2019

`config/car`: Train, validate, and test on TREC CAR

`config/antique`: Train, validate, and test on ANTIQUE

**Models**

`config/conv_knrm`: Use the ConvKNRM model

`config/vanilla_bert`: Use the Vanilla BERT model

## Citation

```
@inproceedings{macavaney:sigir2020-cl,
  author = {MacAvaney, Sean and Nardini, Franco Maria and Perego, Raffaele and Tonellotto, Nicola and Goharian, Nazli and Frieder, Ophir},
  title = {Training Curricula for Open Domain Answer Re-Ranking},
  booktitle = {Proceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval},
  year = {2020}
}
```

## Data

| Abbreviation | Definition |
|--------------|------------|
| trecdl | [TREC Deep Learning](https://arxiv.org/pdf/2003.07820.pdf) dataset |
| car | [TREC Complex Answer Retrieval](https://trec.nist.gov/pubs/trec26/papers/Overview-CAR.pdf) dataset |
| antique | [ANTIQUE](https://arxiv.org/pdf/1905.08957.pdf) dataset |
| cknrm | [Conv-KNRM](http://www.cs.cmu.edu/~./callan/Papers/wsdm18-zhuyun-dai.pdf) model |
| vbert | [Vanilla BERT](https://arxiv.org/pdf/1904.07094.pdf) model |
| pair | pairwise training |
| pair_recip | pairwise training w/ Reciprocal rank heuristic |
| pair_norm | pairwise training w/ Normalized score heuristic |
| pair_kde | pairwise training w/ Kernel Density Estimation (KDE) heuristic |
| point | pointwise training |
| point_recip | pointwise training w/ Reciprocal rank heuristic |
| point_norm | pointwise training w/ Normalized score heuristic |
| point_kde | pointwise training w/ Kernel Density Estimation (KDE) heuristic |

### TREC-formatted run files

Download: [Google Drive](https://drive.google.com/file/d/1Kq-P-mRqgPAn4Yob12cLkhoVuSlNVyWe/view?usp=sharing) (452MB)

*([Tip for downloading large Google Drive files using wget](https://medium.com/@acpanjan/download-google-drive-files-using-wget-3c2c025a8b99))*

| File Name                       | MD5                                |
|---------------------------------|------------------------------------|
| `trecdl-cknrm-pair.run`         | `314d25047fc622303a5e14f741f9828d` |
| `trecdl-cknrm-pair_recip.run`   | `e4fe1751ccbe89154db10282387528b9` |
| `trecdl-cknrm-pair_norm.run`    | `4ffe3b823adb9c7093ab18d47f9195c0` |
| `trecdl-cknrm-pair_kde.run`     | `f19153781e62e7a7d1c87ad8314a27ff` |
| `trecdl-vbert-point.run`        | `c5c8680ac0820cd0c75b8d517c326116` |
| `trecdl-vbert-point_recip.run`  | `c8b014ddd2764c7abd13039942759760` |
| `trecdl-vbert-point_norm.run`   | `2f10ec55d1fbb9ce570247b9de400b11` |
| `trecdl-vbert-point_kde.run`    | `e61d92d66187e145a592d63386d53b0e` |
| `trecdl-vbert-pair.run`         | `9e23915a8bddb19cf0e16ad450942fb0` |
| `trecdl-vbert-pair_recip.run`   | `af6e5ba49f57f0d45d95ed7bf1e217c2` |
| `trecdl-vbert-pair_norm.run`    | `0d31c3eac042a7d5b30775e2dadbaac8` |
| `trecdl-vbert-pair_kde.run`     | `385db9f2cce6c41bbb09c5253097afb7` |
| `car-cknrm-pair.run`            | `eb526580239e464ae4ca9dd78eb07ee8` |
| `car-cknrm-pair_recip.run`      | `4923ca47cf09508b21e88c2021d05860` |
| `car-cknrm-pair_norm.run`       | `8bcbefe8e4db271aac4ac8b9169ee0e1` |
| `car-cknrm-pair_kde.run`        | `27234ff34c46f48a070daf9624d64fc2` |
| `car-vbert-point.run`           | `d3d1df45c0200c2f7aa7ebceae7928f3` |
| `car-vbert-point_recip.run`     | `26599d29392d2029f5f52eca0c2fe7ae` |
| `car-vbert-point_norm.run`      | `9efc8fcecc1d1c6f62b7c7e608083659` |
| `car-vbert-point_kde.run`       | `ef4dfaee1a5aeee938551d57f0ac2a4f` |
| `car-vbert-pair.run`            | `17c9d2f7292af19e92623ba2b86f8107` |
| `car-vbert-pair_recip.run`      | `e2fd421381ed4a8e912be0969dcf2b75` |
| `car-vbert-pair_norm.run`       | `fc6d5d26844d95f3532659470970454a` |
| `car-vbert-pair_kde.run`        | `8c3772c68f7e738beb352b59f4fead3a` |
| `antique-cknrm-pair.run`        | `a43891254f5c5d05ceef9a59211dd8c7` |
| `antique-cknrm-pair_recip.run`  | `8442bc384fc39ce7629680da50210515` |
| `antique-cknrm-pair_norm.run`   | `85fc256b7c3a94e5b1dadf431500d294` |
| `antique-cknrm-pair_kde.run`    | `a84394d702c4c8e7ac251766d966694e` |
| `antique-vbert-point.run`       | `f4a1deffd2ce15ca2adb123bb6ce3d1a` |
| `antique-vbert-point_recip.run` | `e0e2fcf1e7656ca5dc8aa13f8b272013` |
| `antique-vbert-point_norm.run`  | `1eebf63b7581408386a0eb5c9e0cc986` |
| `antique-vbert-point_kde.run`   | `a4d061f5d03c0aef4b8aa64a05b882be` |
| `antique-vbert-pair.run`        | `d3cb2ec22bfdec8280a222d005f9c3b3` |
| `antique-vbert-pair_recip.run`  | `b5104270af30b34d9c60ddd79a3ecc95` |
| `antique-vbert-pair_norm.run`   | `9735ca112961142344111939917b7e33` |
| `antique-vbert-pair_kde.run`    | `d6d4627952c49d9898232d4a176e1890` |


### Weight files
 
 Download: [Google Drive](https://drive.google.com/file/d/1qKDpPX4sZDHNaY_4GIpAsfWQdTdXoxS4/view?usp=sharing) (12GB)

 *([Tip for downloading large Google Drive files using wget](https://medium.com/@acpanjan/download-google-drive-files-using-wget-3c2c025a8b99))*
 
| File Name                     | MD5                                |
|-------------------------------|------------------------------------|
| `trecdl-cknrm-pair.p`         | `411d36ee06c611266461e4af196a315b` |
| `trecdl-cknrm-pair_recip.p`   | `f4ac98b5cfdc3cb24c61e772fc9d93ce` |
| `trecdl-cknrm-pair_norm.p`    | `c1bacf5e88ed6b7dd9e18c6d25a2a9c0` |
| `trecdl-cknrm-pair_kde.p`     | `544a03268b4f33d04b96ffabcc4fdf0e` |
| `trecdl-vbert-point.p`        | `9f3c39b1f0f08ae046010172e851c2ee` |
| `trecdl-vbert-point_recip.p`  | `1b2b4f869c16a67eb5720774f0967aa8` |
| `trecdl-vbert-point_norm.p`   | `82094d85399ffd267ee0110947bb5848` |
| `trecdl-vbert-point_kde.p`    | `a7c247793ca73b2dd276d12ab918f8b5` |
| `trecdl-vbert-pair.p`         | `d9b659385ac46f282adc461514935b30` |
| `trecdl-vbert-pair_recip.p`   | `0a8ea24695745106e701e0a596ba2283` |
| `trecdl-vbert-pair_norm.p`    | `ed9592a10a012bd6e0081b4d18a38da8` |
| `trecdl-vbert-pair_kde.p`     | `a6aa759130a7ac5ae9bf8119ed760e0f` |
| `car-cknrm-pair.p`            | `83879543fa1c236de1d3fc03651438c6` |
| `car-cknrm-pair_recip.p`      | `ef7e705b7658cdc52f363a37d2b236cc` |
| `car-cknrm-pair_norm.p`       | `b8535b741710f21ec6c725047220f968` |
| `car-cknrm-pair_kde.p`        | `31d7bcf1f351fcb89549c4c0cf83744b` |
| `car-vbert-point.p`           | `a7930504eb0aaa31cdba73815c91f7bd` |
| `car-vbert-point_recip.p`     | `a24bac3be23ea94fd431181cc9ca3050` |
| `car-vbert-point_norm.p`      | `d47745d089a55ae91ebb1b77903a432d` |
| `car-vbert-point_kde.p`       | `805e234356d36de1ee2835242002643c` |
| `car-vbert-pair.p`            | `c1de35c7fc6305b3d5b7420cd6db7b64` |
| `car-vbert-pair_recip.p`      | `688a0c064355bcd614c65208201c616a` |
| `car-vbert-pair_norm.p`       | `2427c4699dd66f905633957a9b75faeb` |
| `car-vbert-pair_kde.p`        | `b5a77304863c325e67c63d06790165ab` |
| `antique-cknrm-pair.p`        | `91629ef0050dde4d979cdd8245c0b664` |
| `antique-cknrm-pair_recip.p`  | `36b15087ed23b84de8016dcc6e3f5de6` |
| `antique-cknrm-pair_norm.p`   | `ac758f2742ba5f604a9eaff6f946d3fc` |
| `antique-cknrm-pair_kde.p`    | `fdc0dfddff52e100b6153be69e501045` |
| `antique-vbert-point.p`       | `8dfc1eaf4ba36f72cf296a000901c4b3` |
| `antique-vbert-point_recip.p` | `3ce45b5af1ce9cfd937c4e8e6fb0e29c` |
| `antique-vbert-point_norm.p`  | `d7918f160cb6e6cc933382b2568a8cc5` |
| `antique-vbert-point_kde.p`   | `348a1be2f5e3b470eda6d3d6a2aba747` |
| `antique-vbert-pair.p`        | `6f99c4f531827ac178ad7edea019c84c` |
| `antique-vbert-pair_recip.p`  | `46c3c82f35f2b777d3c587f4d9aa8dce` |
| `antique-vbert-pair_norm.p`   | `c9941aa7bb13090be6ad3420442b23d1` |
| `antique-vbert-pair_kde.p`    | `c3aa767603fecdc5e372e7c6c105108d` |
