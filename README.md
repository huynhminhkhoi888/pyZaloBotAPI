[![PyPi Package Version](https://img.shields.io/badge/pypi-v.0.1.0-blue)](https://pypi.python.org/pypi/pyTelegramBotAPI)
[![Supported Python versions](https://img.shields.io/badge/python-3.8%20%7C%203.9%20%7C%203.10%20%7C%203.11-blue)](https://pypi.python.org/pypi/pyTelegramBotAPI)

# <p align="center">pyZaloBotAPI

## Language Selection / Chọn Ngôn Ngữ

- [English](#english)
- [Tiếng Việt](#ti%E1%BA%BFng-vi%E1%BB%87t)

---

## English
### Content
* [Introduction](#introduction)
* [Getting started](#getting-started)

### Introduction

Hello everyone, my name is KhoiHuynh1109. Because when using **Zalo**, I met a friend who used his account as a bot that is actually similar to a **Telegram** bot with the [`pyTelegramBotAPI`](https://github.com/eternnoir/pyTelegramBotAPI) module. So, I was very interested and consulted his method and decided to create a module that looks exactly like a `telebot` called `zalobot` but has certain limited functions due to processing requirements as well as limitations about **Zalo's** mechanism.

### Getting started
This API is tested with Python 3.8-3.11 and Pypy 3. There are two ways to install the library:

* Installation using pip (a Python package manager):
```
pip install pyZaloBotAPI
```
* Installation from source (requires git):
```
pip install git+https://github.com/huynhminhkhoi888/pyZaloBotAPI.git
```
It is generally recommended to use the first option.

*While the API is production-ready, it is still under development and it has regular updates, do not forget to update it regularly by calling*
```
pip install pyZaloBotAPI --upgrade
```


## Tiếng Việt
### Nội dung 
* [Giới thiệu](#giới-thiệu)
* [Bắt đầu](#bắt-đầu)
* [Các hàm cơ bản](#các-hàm-cơ-bản)
### Giới thiệu
Xin chào mọi người, mình tên KhôiHuynh1109. Bởi vì khi sử dụng **Zalo**, tôi gặp một người bạn sử dụng tài khoản của mình làm bot thực sự giống với bot **Telegram** với mô-đun [`pyTelegramBotAPI`](https://github.com/eternnoir/pyTelegramBotAPI). Vì vậy, tôi rất thích thú và tham khảo ý kiến ​​phương pháp của anh và quyết định tạo ra một mô-đun trông giống hệt một `telebot` tên là `zalobot` nhưng có một số chức năng hạn chế nhất định do yêu cầu xử lý cũng như hạn chế về cơ chế **Zalo**. 
### Bắt đầu
API này đã được thử nghiệm với Python 3.8-3.11 và Pypy 3. Có hai cách để cài đặt thư viện: 
* Cài đặt bằng pip (trình quản lý gói Python):
```
pip install pyZaloBotAPI
```
* Cài đặt từ nguồn (yêu cầu git):
```
pip install git+https://github.com/huynhminhkhoi888/pyZaloBotAPI.git
```
Nói chung nên sử dụng tùy chọn đầu tiên.

*Mặc dù API đã sẵn sàng để sản xuất nhưng nó vẫn đang được phát triển và có các bản cập nhật thường xuyên, đừng quên cập nhật thường xuyên bằng cách gọi* 
```
pip install pyZaloBotAPI --upgrade
```
### Các hàm cơ bản

Để tiến hành code những bước cơ bản cho con bot của bạn đầu tiên và tất yếu nhất là việc khởi tạo và cung cấp những thứ cần thiết nhất liên quan đến zalo như: **`cookie`**, **`imei`**, **`grid`** và hơn nữa là **`admin_id`**

*Ngoài lề 1 tí về lí do cần có **`admin_id`** bởi do việc sử dụng chính cookie tài khoản của mình thay vì 1 con bot riêng biệt (nếu có bằng acc clone) nên đôi khi chính mình có thể nhắn tin hay sử dụng bot vì thế mà kết quả trả về **`uidFrom`** từ **API** của zalo là **`0`** nên không biết reply tin nhắn như thế nào vì thế mà cần cung cấp dữ liệu **`admin_id`***

**Đầu tiên để khởi tạo bot mọi người có thể xem code dưới đây:**
```python
import zalobot
bot = zalobot.ZaloBot(cookies="YOUR_COOKIE_ZALO")
```
Để lấy cookies zalo nếu mọi người chưa biết hoặc chưa từng lấy bao giờ thì làm theo cách sau:
* Đối với người sử dụng máy tính:

  Mọi người vào trình duyệt có thể là **Chrome** hoặc **Cốc Cốc**, sau đó vào website **[chat.zalo.me](https://chat.zalo.me)** bật F12 và đăng nhập. Nói thì có hơi mất thời gian, mọi người có thể xem qua đoạn video ngắn này cho dễ hiểu: **[Click vào đây](https://www.veed.io/view/c4876d82-017b-472e-bb97-bd126a982492?panel=share)**
