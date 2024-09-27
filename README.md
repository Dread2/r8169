Notes: 
LAN WAKE-UP Signal (When CardB_En=0, bit2 Config3).
This signal is used to inform the motherboard to execute the
wake-up process. The motherboard must support Wake-On-LAN
(WOL). There are 4 choices of output that may be asserted from the
LANWAKE pin (active high, active low, positive pulse, and
negative pulse). We can configure the LANWAKE output via two
CONFIG bits: LWACT (Config1.4) and LWPTN (Config4.2).
LWAKE Output LWACT
0 1
LWPTN 0 Active high Active low
1 Positive pulse Negative pulse
The default output is an active high signal. Once a PME event is
received, the LANWAKE and PMEB assert at the same time if the
LWPME (bit4, CONFIG4) is set to 0. If the LWPME is set to 1, the
LANWAKE asserts only when PMEB asserts and ISOLATEB is
low

Ensure, WOL properly works upon bit-set. Need to test along several R8169 models including,
R8169, R8169S, R8169S-32, R8169-64, R8169-SB, SB-LF, and SC
