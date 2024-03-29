# ezminingrig v0.1alpha

## Caveat :construction:

This rig will not make you rich :fox_face:. Do this with no warranty and no guarantees.

## Why Even? :thinking:

This is an easy way to get started mining and learn about mining with a GPU in early 2021. It is not the best way to mine. It is a stepping stone you can use on the way to making better mining rigs later. 

The concept is it is easy to make and has a worse ROI than better designed rigs but has less parts to source and takes a lot less time and skill to make. For a cool and profitable build start with this one using old 5700XTs (if you can get 8 5700XTs at a good price do this instead!):
https://www.youtube.com/watch?v=KQSiReNcBeA

This thing is also low noise, compact and has nice lights (well those just come with the GPUs...pretty RGB). The parts are composeable, modular and can be reused for other hobbiest things. You might even consider upgrading the NUC and the other stuff if you plan to eventually do that and move the GPU to a more involved rig.


## BOM ( $2515.11 total ) :hammer:
- Physical ( Cost $2515.11 )
  - Intel i3 NUC
    - https://www.microcenter.com/product/631454/intel-nuc-10-performance-kit-intel-core-i3-processor ( $349.99 ) 
  - NVME riser for GPU :ski: ( I call this "the sled" thoughout this document )
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
  - A spare ethernet connection to plug the nuc into (you could do wifi, but you'll have to look at the mineros settings on how to set that in the config.js )
- Digital ( Cost $0 )
  - Balena Etcher 
    - https://www.balena.io/etcher/
  - Mining OS (note... you can opt to use HiveOS and get about 20 M/Hs more out of any card with Overclocking...)
    - https://minerstat.com/software/mining-os 
  - Ethereum wallet
    - send yourself the public address for the ETH account you will send mining spoils to
- (YVT) Your Valuable Time required to make this 
  - 4 hrs tops   

## Quick Instructions :paperclip: <- click the paperclip for support, it talks
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
- Power the nuc on and mash F10 while it is turning on so you get a boot selection menu. Choose boot off USB stick
- Configure the worker in minerstat (using a web browser on another computer) to
  - Mine ethash (consider using nbminer for this)
  - Send to a pool (consider nanopool https://eth.nanopool.org/)
    - get the pool address, e.g. eth-us-west1.nanopool.org:9999, and save it in minerstat in the address editor and gitve it a name you can remember, e.g. NANO-ETH
  - Send to a wallet
    - save an entry in the address editor with your public ETH address for your wallet you will send your profit to
- After saving the changes to your worker you should see that worker restart and you can watch it start mining. Minerstat will indicate when it is getting shares and you can also log in to a terminal on the box remotely to see it go with lots of output. When it gets shares you get fractions of your minimum payout. When that threshold is reached the pool sends to your wallet and you have Ether. 
- If you are using nanopool you can put your address in nanopool to see the progress towards your payout as it mines. I also recommend configuring the minimum payout to be 0.05

## Tested Configurations (specs with no default settings and no custom overclock settings in MinerOS) :gear:
| GPU       | Ethash HashRate | Ethash HashRate Overclocked (New!) |
| --------- | --------------- | ---------------------------------- |
| RTX 3090  | 107 MH/s        | 119 MH/s                           | 
| RTX 3070  | 52 MH/s         | 60 MH/s                            |

## ROI (using current ETH price 1439 for dollar conversions ) :money_with_wings: <- your money is flying away. I warned you....
  - Gross income
    - Daily $8.38
  - Electrity Expenses (using example of $0.10 / kWh )
    - Daily $1.80 
  - Net Income 
    - Daily $5.51
  - Break Even Point ( Wait you're not hodling !? )
    - $2515 / ( $6.58/day ) = 382 days

## Why is this even a thing? :saxophone:
I happen to have this rig because I had most of the parts lying around. Then I got a GPU and a PSU with the intention of mining and immediately thought of all the ways I could hook them up. I like hooking the rigs up some times this way because it is easy to do and makes unused parts go to work. :necktie: 

## Updates :honeybee:
I tried HiveOS and can now recommend it besides some security concerns. MinerOS will get you started but HiveOS can get you better hashrates:
- https://hiveos.farm/

## A note on profitibility and taking this further :moneybag:
This kind of rig is actually very capable of making more than listed above. ETH has been on a real bull run... and this is crypto you're getting! You'll want to HODL it and/or reinvest it and really, many things could possibly go right if you don't suck at DeFi...

I currently have a mixed rig which is made up of a misfit hodgepodge that includes 2 of these sled style rigs, 1 crazy inefficient PowerEdge r910, and one kind of half full sluice-style efficient setup that is more similar to the one in the mining chamber video.

I currently have a total hashrate for the whole farm of 385 MH/s, and that is enough to make $111 every 3 days during this bull run. This is nothing compared to the beefy setups people often get into and you will likely want to go bigger as long as you can safely expand.

I would recommend tapping into the mining communities that exist by going to the Discord servers for the best YouTubers on this. That includes RedPanda Mining, MiningChamber, VoskCoin, etc. There's a lot out there. There videos are good and they can show you how to wire things and not cause a fire, which is really an important thing to do.

Don't burn your building down, use renewable energy and try capturing a little of the current goldrush here while it is still worth it.

Currently mining is profitible, and even when it isn't immediately... HODL. 

## But I'm not technical! :confused:
All the more reason to get into this... Enjoy learning something new... maybe pair up with someone that is... may also be the beginning of a beautiful friendship.
Be careful though... your valuable time :watch: is at stake... and you may be left with a ... learning experience :lemon:. If you are the kind of person that can accept that, and see it as not an entirely bad or fruitless thing :cocktail:, then this guide was made for you.
