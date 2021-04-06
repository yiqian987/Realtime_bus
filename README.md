# Realtime_bus
通过北京公交集团api封装后的查询接口
# 举几个例子
```
bus = Busstat()
```
## bus.getNumbers("368")
```
[
    {
        'lineId': '000014286687271',
        'lineName': '368外',
        'direction': '1',
        'firstStationName': '城南嘉园北',
        'lastStationName': '城南嘉园北',
        'serviceTime': '5: 00-21: 30',
        'isNight': '0',
        'isSinglePrice': '0',
        'isCrossCity': '0',
        'startPrice': '2',
        'maxPrice': '0',
        'lineLength': '53.000',
        'subcategorytxt': '公交线路',
        'caption': '368外(城南嘉园北-城南嘉园北)',
        'id': '000014286687271',
        'dataid': '000014286687271'
    },
    {
        'lineId': '000014286687281',
        'lineName': '368内',
        'direction': '1',
        'firstStationName': '航天桥西',
        'lastStationName': '航天桥西',
        'serviceTime': '5: 00-21: 30',
        'isNight': '0',
        'isSinglePrice': '0',
        'isCrossCity': '0',
        'startPrice': '2',
        'maxPrice': '0',
        'lineLength': '49.000',
        'subcategorytxt': '公交线路',
        'caption': '368内(航天桥西-航天桥西)',
        'id': '000014286687281',
        'dataid': '000014286687281'
    }
]
```
## bus.getStopName("368", "苏州桥南")
```
[
    {
        '368外(城南嘉园北-城南嘉园北)': {
            'stationId': '110100016367062',
            'stopNumber': '41',
            'stopName': '苏州桥南',
            'lineId': '000014286687271'
        }
    },
    {
        '368内(航天桥西-航天桥西)': {
            'stationId': '110100014901053',
            'stopNumber': '7',
            'stopName': '苏州桥南',
            'lineId': '000014286687281'
        }
    }
]
```
## bus.getGpsInfo("74", "苏州桥南")
```
[
    {
        '74(颐和园新建宫门-菜户营西路)': [
            {
                'distance': 1078,
                'stationleft': 2,
                'bus_number': '最近一辆车'
            },
            {
                'distance': 4978,
                'stationleft': 9,
                'bus_number': '第2辆车'
            }
        ]
    },
    {
        '74(菜户营西路-颐和园新建宫门)': [
            {
                'distance': 273,
                'stationleft': 0,
                'bus_number': '最近一辆车'
            },
            {
                'distance': 1958,
                'stationleft': 2,
                'bus_number': '第2辆车'
            },
            {
                'distance': 6140,
                'stationleft': 5,
                'bus_number': '第3辆车'
            }
        ]
    }
]
```
