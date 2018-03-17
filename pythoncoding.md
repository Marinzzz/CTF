# python中的各种编码

## 1.url编码
> import urllib
>
> a="adsasd"
>
> b=urllib.unquote(b)
>
> c=urllib.quote(a)

## base系列

> import base64
> 
> b64.base64decode()
>
> b64.base64encode()
> 
## ascii编码
> 10进制ord() & chr()
>
> 16进制 
>
> ```python
> import binascii
> a='1111'
> b=binascii.b2a_hex(a)#b='31313131'
> c=binascii.unhexlify(b)#c=1111
> ```
>
> 
