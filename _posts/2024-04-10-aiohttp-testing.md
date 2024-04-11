---
layout: post
title: aiohttp testing
categories: testing
tags: [testing,python]
---

# Roblox Picture Getter!

No web scraping with this one boys

~~~python
import json,aiohttp,asyncio

async def bruh():
    async with aiohttp.ClientSession() as session:
        username  = "Roblox"
        url = "https://users.roblox.com/v1/usernames/users"
        userIdRequestJSON = json.dumps({"usernames": [username], "excludeBannedUsers": True})
        headers = {
            "accept": "application/json",
            "Content-Type": "application/json"
        }

        async with session.post(url,data=userIdRequestJSON,headers=headers) as resp:
            userIdReqContent = json.loads(await resp.text())
            userId = userIdReqContent["data"][0]["id"]

        iconImageRequestUrl = (f"https://thumbnails.roblox.com/v1/users/avatar-headshot?userIds={userId}&size=420x420&format=Png&isCircular=false")
        async with session.get(iconImageRequestUrl) as resp:
            iconImageReqContent = json.loads(await resp.text())
            imageUrl = iconImageReqContent["data"][0]["imageUrl"]
            print(imageUrl)

asyncio.run(bruh())
~~~

ok thaats it
