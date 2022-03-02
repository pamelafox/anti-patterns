# anti-patterns

A repo to backup the assertions in my PyCon 2022 talk

## Usage

```console
$ pip install -r requirements.txt
$ python suite.py
```

## Results
                                               
```default
┏━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━┳━━━━━━━━━┳━━━━━━━━━┳━━━━━━━━━┳━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━┓
┃ Pattern ┃                                    Benchmark ┃ Repe… ┃ Min     ┃ Max     ┃ Mean    ┃ Min (+)         ┃ Max (+)         ┃ Mean (+)        ┃
┡━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━╇━━━━━━━━━╇━━━━━━━━━╇━━━━━━━━━╇━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━┩
│       1 │                          Copy slice to Local │ 25    │ 0.221   │ 0.224   │ 0.222   │ 0.165 (25.4%)   │ 0.169 (24.3%)   │ 0.166 (25.2%)   │
│       2 │                           Copy name to Local │ 25    │ 0.124   │ 0.127   │ 0.126   │ 0.098 (21.1%)   │ 0.099 (22.2%)   │ 0.099 (21.7%)   │
│       3 │                      Copy dict item to Local │ 25    │ 0.254   │ 0.256   │ 0.255   │ 0.097 (61.9%)   │ 0.098 (61.7%)   │ 0.097 (61.9%)   │
│       4 │                     Copy class attr to Local │ 25    │ 0.222   │ 0.230   │ 0.225   │ 0.075 (66.1%)   │ 0.077 (66.7%)   │ 0.076 (66.1%)   │
│       5 │ Importing specific name instead of namespace │ 25    │ 0.000   │ 0.000   │ 0.000   │ 0.000 (4.5%)    │ 0.000 (34.1%)   │ 0.000 (14.1%)   │
│       6 │     Slicing with memoryview instead of bytes │ 25    │ 0.001   │ 0.001   │ 0.001   │ 0.001 (36.3%)   │ 0.001 (33.7%)   │ 0.001 (35.6%)   │
│       7 │              **Kwargs for known keyword args │ 25    │ 0.000   │ 0.000   │ 0.000   │ 0.000 (15.1%)   │ 0.000 (19.2%)   │ 0.000 (17.3%)   │
│       8 │                               Tiny Functions │ 25    │ 0.000   │ 0.000   │ 0.000   │ 0.000 (71.5%)   │ 0.000 (68.5%)   │ 0.000 (69.7%)   │
│       9 │                   Class instead of dataclass │ 25    │ 0.016   │ 0.016   │ 0.016   │ 0.005 (70.9%)   │ 0.005 (70.2%)   │ 0.005 (70.4%)   │
│      10 │              Namedtuple instead of dataclass │ 25    │ 0.015   │ 0.016   │ 0.016   │ 0.006 (58.2%)   │ 0.007 (56.9%)   │ 0.007 (57.5%)   │
│      11 │                  class instead of namedtuple │ 25    │ 0.006   │ 0.007   │ 0.007   │ 0.005 (28.0%)   │ 0.005 (30.1%)   │ 0.005 (29.1%)   │
│      12 │                        dict instead of class │ 25    │ 0.005   │ 0.005   │ 0.005   │ 0.003 (31.7%)   │ 0.004 (30.6%)   │ 0.003 (32.9%)   │
└─────────┴──────────────────────────────────────────────┴───────┴─────────┴─────────┴─────────┴─────────────────┴─────────────────┴─────────────────┘
```
