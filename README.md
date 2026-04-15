# <img src="https://play-lh.googleusercontent.com/ajQIrBd5NdmqysPxJ5b5XYF8_F5YiRQbYkxjl986_mM0NQos70Chd3_OzyecJ_EBCQ=s48-rw" width="50" style="vertical-align:middle;" /> hide_online.py

> Mobile-API for [Hide Online](https://play.google.com/store/apps/details?id=com.hitrock.hideonline) a mobile hide and seek shooter built on [PlayFab](https://playfab.com).

## Quick Start

```python
from hide_online import HideOnline

hide_online = HideOnline()
response = hide_online.register()
hide_online.login_with_session_ticket(response["data"]["SessionTicket"])
```

## Usage

### Authentication

```python
# Register a new anonymous account
response = hide_online.register()
session_ticket = response["data"]["SessionTicket"]

# Login with session ticket
hide_online.login_with_session_ticket(session_ticket)
```

### Player

```python
hide_online.get_account_info()
hide_online.set_nickname("Hero")
hide_online.get_server_time()
hide_online.get_photon_token()
hide_online.get_title_data()
```

### Equipment

```python
hide_online.equip_items(
    skin="s_male1a",
    weapon="w_rifle3b",
    pose="p_1",
    avatar="a_96",
    emoji="e_0"
)
```

### Store

```python
hide_online.get_store_items(store_id="General")
```

### Gifts & Rewards

```python
# Check and claim a gift
hide_online.check_if_has_gift(gift_name="gift_01")
hide_online.activate_gift_offer(gift_name="gift_01")
hide_online.open_gift_loot_box(gift_name="gift_01")

# Claim video ad reward
hide_online.get_video_ad_reward()
```

## API Reference

| Method | Description |
|---|---|
| `register()` | Register a new anonymous account |
| `login_with_session_ticket(session_ticket)` | Authenticate with a session ticket |
| `get_account_info()` | Get your player profile |
| `set_nickname(nickname)` | Set your nickname |
| `get_server_time()` | Get current server time |
| `get_photon_token()` | Get Photon authentication token |
| `get_title_data(keys)` | Get hide_online config data |
| `get_store_items(store_id)` | Get store listings |
| `equip_items(skin, weapon, pose, avatar, emoji)` | Equip cosmetic items |
| `check_if_has_gift(gift_name)` | Check if a gift is available |
| `activate_gift_offer(gift_name)` | Activate a gift offer |
| `open_gift_loot_box(gift_name)` | Open a gift loot box |
| `get_video_ad_reward()` | Claim a video ad reward |
