# L04E02: Parse command top
Vytvořte modul `parse_top.py` obsahující funkci `parse_top(path)`, jejíž parametr `path` je řetězec s cestou k souboru, který obsahuje výstup příkazu `top`.

Tato funkce ze souboru načte běžící příkazy a do seznamu uloží pro každý příkaz tuple ve tvaru: (PID, USER, %CPU, %MEM, COMMAND).

Snažte se nejvíce využít regulární výrazy.

```python
from parse_top import parse_top

data = [
    ("10", "root", "0,3", "0,0", "rcu_sched"),
    ("877", "root", "6,6", "0,8", "Xorg"),
    ("1209", "george", "0,3", "0,1", "kded5"),
    ("1258", "george", "0,3", "0,2", "kactivitymanage"),
    ("1266", "george", "6,3", "0,8", "kwin_x11"),
    ("1270", "george", "2,0", "3,0", "plasmashell"),
    ("1349", "george", "5,0", "5,0", "thunderbird"),
    ("1379", "george", "0,3", "0,0", "dbus-daemon"),
    ("1633", "george", "1,3", "10,1", "chrome"),
    ("1680", "george", "0,3", "2,0", "chrome"),
    ("1746", "george", "0,3", "0,0", "at-spi2-registr"),
    ("315498", "george", "2,0", "10,0", "chrome"),
    ("328718", "george", "6,3", "1,7", "konsole"),
    ("328731", "george", "0,7", "0,1", "top"),
]

output = parse_top("top.txt")
assert data == output
```