## smfucker

基于SM.SM图床的命令行小工具，第一次使用会要求登录，会在当前文件目录下生成一个config文件，保存token，后面就不会再要求登录了，最主要的功能还是处理md文件。

### 安装教程

```shell
pip install smfucker
```

https://pypi.org/project/smfucker/，后续可能会更新，如果有bug的话。

### 使用方法

使用-h参数，查看所有命令。

```sh
C:\Users\hp>smfucker -h
usage: smfucker [-h] [-f FILE] [--history] [-d DATE] [-n NAME] [--upload UPLOAD] [--delete DELETE] [-l] [--user] [-v]

optional arguments:
  -h, --help            show this help message and exit
  -f FILE, --file FILE  Point to a md file
  --history             look all history
  -d DATE, --date DATE  search by date
  -n NAME, --name NAME  search by name
  --upload UPLOAD       upload by file path
  --delete DELETE       delete by hash
  -l, --login           login
  --user                get user profile
  -v, --version
```



#### 生成修改后的md文件

将md中的所有本地图片都上传到图床中，然后生成新的md文件，需要到对应md文件的目录下执行命令。

```sh
D:\>smfucker -f 文件名称
```

#### 查看user信息

```sh
D:\>smfucker --user
please input your user name:The_Itach1
please input your password:
+-------------------------------------+
|          SM.MS User Profile         |
+----+------------+-------------------+
| id |  project   |       value       |
+----+------------+-------------------+
| 0  |  username  |     The_Itach1    |
| 1  |    role    |        user       |
| 2  |   email    | 2507709326@qq.com |
| 3  | disk_usage |      22.44 MB     |
| 4  | disk_limit |      5.00 GB      |
+----+------------+-------------------+
```

#### 查看所有上传历史

```sh
D:\>smfucker --history
+------------------------------------------------------------------------------------------------------------------------------------------------+
|                                                                 SM.MS History                                                                  |
+-----+----------------------------------+----------------------------------------------------+----------------------------+---------------------+
|  id |             filename             |                        url                         |            hash            |      created_at     |
+-----+----------------------------------+----------------------------------------------------+----------------------------+---------------------+
|  0  | Snipaste_2023-02-23_12-52-59.png | https://s2.loli.net/2023/02/25/QU8A1fEqPbB2DJW.png | zUAFqjyemo9PkdxHtvS7Q4N6Y5 | 2023-02-25 22:41:49 |
|  1  | Snipaste_2023-02-14_10-21-40.png | https://s2.loli.net/2023/02/25/UQELKS4PXhDHimd.png | fnRadQXDFe8wlOLMmubZv2qxig | 2023-02-25 22:38:46 |
|  2  | Snipaste_2023-02-14_10-21-40.png | https://s2.loli.net/2023/02/23/ksYAfNMlvjbEGVF.png | 4klJo1KCizjV3f9e5BptMIWEYy | 2023-02-23 22:37:26 |
|  3  | Snipaste_2023-02-23_12-52-59.png | https://s2.loli.net/2023/02/23/tCou6aIBdFQhYUe.png | PEUFQ3IBLcxJryvRaw5p1OdTGh | 2023-02-23 22:36:49 |
|  4  | Snipaste_2022-09-05_22-39-32.png | https://s2.loli.net/2022/09/05/1FXgutixsOAcV9m.png | ZYd9wqhrieH1VPF8zOEkUo2GTN | 2022-09-05 22:39:45 |
|  5  | Snipaste_2022-09-05_21-02-35.png | https://s2.loli.net/2022/09/05/YdVHCNjhmtwsRQZ.png | lq4oOPvjwZM91p6fzhgyFRexL3 | 2022-09-05 21:02:56 |
|  6  | Snipaste_2022-09-05_11-59-17.png | https://s2.loli.net/2022/09/05/KAQCP6Llu4MYVeG.png | v7kNRq9GcMVyQTgK6SdhU8w3ba | 2022-09-05 11:59:30 |
|  7  | Snipaste_2022-09-04_22-22-18.png | https://s2.loli.net/2022/09/04/NUXxvVHJYBgD31z.png | tk89RXWhEJM6j7d4SaeKAOiYT5 | 2022-09-04 22:22:53 |
|  8  | Snipaste_2022-09-04_18-29-01.png | https://s2.loli.net/2022/09/04/khXnY3tl5PvWr4y.png | P1LMutvlexVnZz6rJY2cidI9CK | 2022-09-04 18:29:48 |
|  9  | Snipaste_2022-09-02_20-02-27.png | https://s2.loli.net/2022/09/02/21jiMNgGRTylQzK.png | 5wuUOcAjBfFnx9hZqtdJER12be | 2022-09-02 20:02:36 |
|  10 | Snipaste_2022-09-02_20-01-40.png | https://s2.loli.net/2022/09/02/xBo9mvP8bnuOV6S.png | daigS52oVYvxDkqBrFKZ6scTP4 | 2022-09-02 20:01:52 |
|  11 | Snipaste_2022-09-02_19-43-35.png | https://s2.loli.net/2022/09/02/zM7icxZCQEUm8NS.png | Hy6VM1wt9pmQv7Rx5l8aESergc | 2022-09-02 19:56:20 |
|  12 | Snipaste_2022-09-02_19-41-13.png | https://s2.loli.net/2022/09/02/tchFQZeUK6CGsJB.png | 8Ly5oUH1nqujTwr2iY79VFOvaR | 2022-09-02 19:48:13 |
|  13 | Snipaste_2022-09-02_19-08-23.png | https://s2.loli.net/2022/09/02/tg3P7j9WcY2fCAK.png | gpKDB4zkj9AUXbvIeJHEqMGrN3 | 2022-09-02 19:08:57 |
|  14 | Snipaste_2022-09-02_16-54-33.png | https://s2.loli.net/2022/09/02/EPdOTRbyjoQAqki.png | UWJwam2nZFREyQTP4bNGtY6qdK | 2022-09-02 16:55:16 |
|  15 | Snipaste_2022-09-02_13-34-09.png | https://s2.loli.net/2022/09/02/FB2Cqk89LHw1Pgi.png | Q6JdDgVco4CtbjSZB1wprzLG23 | 2022-09-02 16:07:47 |
```

#### 根据名称和日期进行查找

```sh
D:\>smfucker --history --date 2022-01-31
+-----------------------------------------------------------------------------------------------------------------------------------------------+
|                                                                 SM.MS History                                                                 |
+----+----------------------------------+----------------------------------------------------+----------------------------+---------------------+
| id |             filename             |                        url                         |            hash            |      created_at     |
+----+----------------------------------+----------------------------------------------------+----------------------------+---------------------+
| 0  |          wl-op-13se.jpg          | https://s2.loli.net/2022/01/31/ktMQEOe8CgB9LJD.jpg | MjATgnGho9kmiVP1rdwlpbY7SN | 2022-01-31 22:31:38 |
| 1  |          wl-op-13se.jpg          | https://s2.loli.net/2022/01/31/ktMQEOe8CgB9LJD.jpg | MjATgnGho9kmiVP1rdwlpbY7SN | 2022-01-31 22:31:38 |
| 2  | Snipaste_2022-01-31_22-05-24.png | https://s2.loli.net/2022/01/31/umdZo97DFijMhGw.png | 1jHZhr7WkV8FzPIeBcxTiwNLMf | 2022-01-31 22:05:36 |
| 3  | Snipaste_2022-01-31_22-05-24.png | https://s2.loli.net/2022/01/31/umdZo97DFijMhGw.png | 1jHZhr7WkV8FzPIeBcxTiwNLMf | 2022-01-31 22:05:36 |
| 4  | Snipaste_2022-01-31_21-53-41.png | https://s2.loli.net/2022/01/31/2CzocvpYatFVE7e.png | evuU6ojlmCTWVKSn4zr8wYkiGg | 2022-01-31 21:54:09 |
| 5  | Snipaste_2022-01-31_21-53-41.png | https://s2.loli.net/2022/01/31/2CzocvpYatFVE7e.png | evuU6ojlmCTWVKSn4zr8wYkiGg | 2022-01-31 21:54:09 |
+----+----------------------------------+----------------------------------------------------+----------------------------+---------------------+
```

#### 删除和单独上传

```sh
--upload file
--delete hash
```



