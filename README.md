# SCJ_Dracoino_Base
Basefirmware for Dracoino Sensor Boards

# Usage
You can youse this to start in developing sensors for LoraWAN applications. It is meant to run on Dracoino Boards. Change anything to your needs.

# devices.h
Define your devices here. You can use the example provided in devices.h.tmpl

# config.h
In this file you can make your local configuration

## LORA_CLK_ERR
Set the CLK_ERR for LMIC lib. On AVR with 8MHz internal 2 seems to be goot.

## INDICATE_LED
GPIO Port for an LED. (Pin 10 on Dracoino boards)

## BAT_MAX
Maximum reading of AnalogRead for battery.

## BAT_MIN
Minimum reading of AnalogRead for battery.

## PINMODEPOWERSAVE
If this is set, all unused pins are configured as outputs. This saves some battery.

## DISABLEBOD
If this is set, Brown Out Detection is disabled. Because Dracoino has onboard voltage regulator BOD makes no sense for them.
BOD also consumes battery.

## LINKCHECKMODE
If this is set, the LoraWAN link check is activated.

## ADRMODE
If this is set, LMIC will work with automatic data rate. Meaning, that the network is able to configure the characteristic of uplink messages (Spreadingfactor, power used, ...).
Check MCCI LoRaWAN LMIC library for details.

# scj_reg.h
This file is meant as a single place for generaly used frames and messages. 
If you add something. please let me know and maybe make a push request to extend them.

## SCJ_PORT_*
Port definitions for easy decode of different types of data. Ports 1 and 224-255 are reserved by LoraWAN specification.

## SCJ_ERR_*
Error Codes.



#define Pinger03
#define MY_PORT             SCJ_PORT_TEMP
#define PINSTATE            OUTPUT
#define LORA_CLK_ERR        2
#define INDICATE_LED        10

#define BAT_MAX             800
#define BAT_MIN             530

#define PINMODEPOWERSAVE
#define DISABLEBOD
#define LINKCHECKMODE
#define ADRMODE