# ezminingrig

## Caveat

I am not a financial advisor. I'm not going to make you rich. I can help you learn things. Do this with no warranty and no guarantees.

## Why?

This is an easy way to get started Mining and learn about mining with a GPU in early 2021. It is not the best way to mine. It is a stepping stone you can use on the way to making better mining rigs later. 

The concept is it is easy to make and has a worse ROI than better designed rigs but has less parts to source and takes a lot less time and skill to make. For a cool and profitable build start with this one using old 5700XTs (if you can get 8 5700XTs at a good price do this instead!):
https://www.youtube.com/watch?v=KQSiReNcBeA

This thing is also low noise, compact and has nice lights. The parts are composeable, modular and can be reused for other hobbiest things. You might even consider upgrading the NUC and the other stuff if you plan to eventually do that and move the GPU to a more involved rig.


## BOM ( $2515.11 total )
- Physical ( Cost $2515.11 )
  - Intel i3 NUC
    - https://www.microcenter.com/product/631454/intel-nuc-10-performance-kit-intel-core-i3-processor ( $349.99 ) 
  - GPU NVME ( I call this "the sled" thoughout this document )
    - https://amzn.to/3q15oTp ( $61.17 )
  - RAM
    - https://www.microcenter.com/product/626749/crucial-8gb-ddr4-2666-pc4-21300-cl19-single-channel-desktop-memory-module---green ( $37.99 )
  - SSD Drive
    - https://www.microcenter.com/product/485877/inland-professional-120gb-ssd-3d-tlc-nand-sata-iii-6gb-s-25-internal-solid-state-drive-(120g) ( $21.99 )
  - USB Thumbdrive
    - https://www.microcenter.com/product/487102/micro-center-16gb-superspeed-usb-31-(gen-1)-flash-drive ( $3.99 )
  - GPU (high tier example)
    - https://www.bestbuy.com/site/evga-geforce-rtx-3090-ftw3-ultra-gaming-24gb-gddr6-pci-express-4-0-graphics-card/6436192.p?skuId=6436192 ( $1869.99 )
  - Power Supply (for 3090)
    - https://www.monoprice.com/product?p_id=18437 ( $169.99 )
  - Another Computer to make the thumbdrive to boot off of
  - A spare keyboard
  - A small screwdriver (philips)  
  - An extra monitor with an HDMI out
- Digital ( Cost $0 )
  - Balena Etcher 
    - https://www.balena.io/etcher/
  - Mining OS
    - https://minerstat.com/software/mining-os 
- (YVT) Your Valuable Time required to make this 
  - 4 hrs tops   

## Quick Instructions
- Open nuc with screwdriver
  - Put in RAM
  - Put in SSD Drive
- Attach ADT Link NVME RG3 Sled to NUC
- Put Graphics card in ADT Link Sled
- Plug in your power supply
  - Connect the motherboard cable on the PSU to the sled according to the instructions on the website  
- Download mining OS https://minerstat.com/download/msos-direct  
- Use Balena Etcher to flash mining OS to Thumbdrive
- Set up an account on minerstat
  - Save your access key in a place you can access it later
  - Make a worker and give it a name. Save that name in a place you can access it later
- Use a text editor to edit the config.js file at the root of the flashed thumbdrive
  - You need to fill out two fields you saved earlier
    - Your access key
    - Your workers name
  - safely eject the thumbdrive
- Put the mining OS thumbdrive in the nuc
- Plug a keyboard and a monitor into the NUC    

## Tested Configurations (specs with no default settings and no custom overclock settings in MinerOS)
| GPU       | Ethash HashRate |
| --------- | --------------- |
| RTX 3090  | 107 MH/s        |
| RTX 3070  | 52 MH/s         |

## ROI (using current ETH price 1439 for dollar conversions )
  - Gross income
    - Daily $8.38
  - Electrity Expenses (using example of $0.10 / kWh )
    - Daily $1.80 
  - Net Income 
    - Daily $5.51
  - Break Even Point ( Wait you're not hodling !? )
    - $2515 / ( $6.58/day ) = 382 days
