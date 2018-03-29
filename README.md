# Asterisk-SetExt-CallerID
Simple Asterisk AGI script for setting CallerID for outgoing calls.

Dialplan sample: ```exten => _X.,n,AGI(set-ext-callerid.pl,${EXTEN})```
