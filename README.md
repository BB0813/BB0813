- 👋 我是BinbimTech
- 一名中职计算机专业二年级在读生
- 👀 目前正在自学前端&后端 力求全栈开发
- 个人主页地址[跳转](https://home.binbim.top/)


from dataclasses import dataclass
from typing import Tuple


class Meta(type):
    def __new__(cls, name, bases, attrs):
        new_cls = super().__new__(cls, name, bases, attrs)
        return dataclass(unsafe_hash=True, frozen=True)(new_cls)


class Bio(metaclass=Meta):
    name        : str = "Dahezhiquan"
    designation : str = "Data Scientist"
    company     : str = "ShopUp"
    base        : str = "Dhaka, Bangladesh"
    blog        : str = "rednafi.github.io/digressions"


class Stack(metaclass=Meta):
    languages   : Tuple[str, ...] = ("Python", "Go", "Shell")
    databases   : Tuple[str, ...] = ("MySQL", "PostgreSQL", "Mongo", "Redis")
    misc        : Tuple[str, ...] = ("Docker", "Celery")
    ongoing     : Tuple[str, ...] = ("Django", "GraphQL")


class Social(metaclass=Meta):
    twitter     : str = "rednafi"
    linkedin    : str = "redowan"

<!---
BB0813/BB0813 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
