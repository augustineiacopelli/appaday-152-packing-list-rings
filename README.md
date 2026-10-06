# 152 Packing List Rings

**AppADay No. 152** | Category: Data Viz (D) | Shipped October 6, 2026

**Live app:** https://augustineiacopelli.github.io/appaday-152-packing-list-rings/
**Portfolio:** https://augustineiacopelli.github.io/appaday/

Packing List Rings builds a packing list for everyone on a trip. Add travelers as adults, kids, or infants, set dates, climate, and setting, and it generates items per person with quantities scaled to trip length. Animated progress rings track each category and traveler until everything is packed.

## How it works

The app has three panels. On a phone they sit behind a sticky Travelers, Trip, and Pack switcher. On a screen wider than 900px they show together, with Travelers and Trip on the left and Pack on the right.

**Travelers.** Save everyone who might come along once, each with a name, a type (adult, child, or infant), male or female, and one of eight colors. A new traveler joins the current trip automatically. Deleting someone who is on the trip asks first, then removes their items too.

**Trip.** Tap travelers in or out, choose departure and return dates, a climate (hot, mild, cold, wet), and a setting (beach, city, outdoors, business). Switch on International for passports, a power adapter, and local currency, and pick the hemisphere so the season is right: a July trip south of the equator is a winter trip. The panel shows the derived season and length, explains anything that blocks generation, and then generates the list.

**Pack.** A large ring shows overall progress, smaller rings show each traveler and the shared items, and colored rings show each category. Rings animate as items are checked, turn green with a checkmark and a single pulse at 100 percent, and disappear when their group empties. Filter by Everyone, Shared, or one traveler, and the list and rings follow. Tap a name to rename it, use the stepper to change a quantity (stepping below one removes the item), add your own items in new categories, hide packed items, uncheck everything in one tap, or regenerate.

## Packing rules

The catalog holds 77 items across clothes, toiletries, electronics, and documents. Each item can be limited by climate, setting, season, traveler type, male or female, and the international switch, and is either packed for each qualifying person or once as a shared item. Quantities scale with the trip: underwear and socks are one per night plus one (up to 8), shirts one per day (up to 7), pants and pajamas one per three days, and toiletries switch from travel size to full size after 5 nights. Women get items such as bras and feminine care products, men get shaving cream and ties for business trips, and infants get onesies, a sleep sack, and their own gear, while diapers, wipes, and bottles are listed once as shared.

On a trip with only one traveler there is nothing to share, so shared items such as toiletries, chargers, and documents are assigned to that person, and the Shared filter and ring step aside. Add a second traveler and those items move back to Shared, keeping their packed checks.

Regenerating rebuilds the list from the current trip settings. Packed checks and renamed items carry over for anything that stays on the list, and items you added yourself are kept.

## Printing

**Print** in the Pack toolbar makes a clean black and white checklist on white paper, with the trip dates, length, climate, setting, and travelers at the top. Choose **By category** for one combined two column list showing whose each item is, or **By person** to start each traveler, and the shared items, on a new page so everyone can check off their own bag. The printout follows the current filter, and items already packed print with their box checked.

## Moving a list to another device

Under Travelers, **Share list link** packs the travelers, trip, and list (packed checks and your own items included) into a link and opens the phone's share sheet, or copies the link where there is no share sheet. Open the link on the other phone or computer, or paste the link or its code into the Import field there. A device with nothing on it simply imports. A device that already has a list asks whether to **Replace** it with the imported one or **Merge**, which keeps what is there, adds new travelers, items, and categories, matches travelers by name and type, and combines matching items so a packed check on either device stays checked. A damaged or partial code is rejected without touching the current list.

## Data and privacy

Everything is stored in your browser's localStorage under `appaday152_v1`. The transfer link carries the list after the # in the address, a part of a URL that browsers never send to a server, so the list travels only through whatever you send the link with. The only network request is for Google Fonts.

## Built with

A single `index.html` of HTML, CSS, and vanilla JavaScript with SVG progress rings. No framework, no build step, no dependencies. It works at 375px and up, uses 44px minimum tap targets, respects reduced motion, and opens full screen with its own icon when saved to a phone's home screen.

---

Part of [AppADay](https://augustineiacopelli.github.io/appaday/), one complete web app shipped every day.
