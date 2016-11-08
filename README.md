# ShopCartLogic
1.用RecyclerView嵌套RecyclerView，
商铺是第一层RecyclerView的item，每间商铺的商品显示是第二层RecyclerView。
2.一层RecyclerView解决问题：
（1）分两种布局去做，第一种布局是含有商铺名字header的item，
第二种是不含有商铺名字no_header的item。
（2）一种布局完成所有操作，具体做法是，记录以同一间商铺id的第一件商品的位置，
然后通过这样的记录在adapter里面去显示和隐藏每个item相应的heade

很明显，每个item都含有商铺名字的header，那下面我就要具体讲讲整个购物车的界面逻辑怎么去做了。

后台数据类型
{
 "message": "查询成功",
 "status": "200",
 "result": [
      {
      "shopId": 2,//店铺
      "shopName": null,//店铺名称
      "cartlist": [//购物车商品
        {
          "id": 2,//购物车
          "shopId": 2,
          "shopName": null,
          "defaultPic": "111.jpg",//默认略缩图
          "productId": 2,//商品
          "productName": null,//商品名称
          "color": null,//颜色
          "size": null,//尺寸
          "price": null,//单价
          "count": null//数量
        },
        {
          "id": 2,//购物车
          "shopId": 2,
          "shopName": null,
          "defaultPic": "111.jpg",//默认略缩图
          "productId": 2,//商品
          "productName": null,//商品名称
          "color": null,//颜色
          "size": null,//尺寸
          "price": null,//单价
          "count": null//数量
        }
      ]
    },
    {
      "shopId": 2,//店铺
      "shopName": null,//店铺名称
      "cartlist": [//购物车商品
        {
          "id": 2,//购物车
          "shopId": 2,
          "shopName": null,
          "defaultPic": "111.jpg",//默认略缩图
          "productId": 2,//商品
          "productName": null,//商品名称
          "color": null,//颜色
          "size": null,//尺寸
          "price": null,//单价
          "count": null//数量
        },
        {
          "id": 2,//购物车
          "shopId": 2,
          "shopName": null,
          "defaultPic": "111.jpg",//默认略缩图
          "productId": 2,//商品
          "productName": null,//商品名称
          "color": null,//颜色
          "size": null,//尺寸
          "price": null,//单价
          "count": null//数量
        }
      ]
    }
  ]
}

From:http://www.jianshu.com/p/6c3328f87fc9
