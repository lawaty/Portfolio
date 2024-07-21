# Mynty Collections Dashboard System
[Mynty.gg](https://mynty.gg)

## Oveview
A Wordpress system contains a smart Arte-based API used to scrape games from ebay and automatically analyzes these games based on price and condition using advanced mathematical statistical analysis to categorize these games into administrator desired categories.

## My Role
> 1. Software Architect
> 2. Full-Stack Developer

## Features
1. `Background Processing`
2. Scrapped and Categorized over a `million game items` so far.
3. Powerful Dashboard to manage `background processes`, review automated categorizing output, and publish games to wordpress database.
4. `Manual Control over everything`
5. `Smart Categorizing` filters out badly categorized items for manual review.
6. `User Collection Feature` allows users to add items to their collection and track their `real-time collection pricing` over time based on price updates and builds a `price graph` shows how his collection value changed over the past 6 months.
7. Controlling Wordpress Woocommerce viewable products from the scrapper dashboard

## Contribution
1. Designed the system and the categorizing solution
2. Designed and implemented the dashboard's front-end
3. Reworked critical Wordpress components to utilize Arte base drastically improved performance.

## Technical Keypoints
1. `Automated Scrapper and Categorizer` based on scrapped items prices, titles, and other meta data
2. `Scrapping` over a million games was a very intensive operation that might still be working in the server background while you read this. Using `background processes with resource limiting was a must` to keep the server healthy.
3. `Categorizer` is a smart statistical decision maker uses system `global analytics` to provide centroids for all system categories. It compares the scrapped items with the existing category centroids and analyzes other item meta information to specify this item condition, packaging, and flagging. 
4. Managing over 30 running background processes from a front-end dashboard in real-time required `queuing back-end services` and `limiting their resources` while providing proper `real-time feedback` to the client app.