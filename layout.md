# flex-direction

* row

  `1` `2` `3`

* row-reverse

  `3` `2` `1`

* column

  `1`

  `2`

  `3`

* column-reverse

  `3`

  `2`

  `1`



# flex-wrap

* nowarp

  `1` `2` `3` `4` `5` `6`

* wrap

  `1` `2` `3` `4` 

  `5` `6`

* wrap-reverse

  `1` `2`

  `3` `4` `5` `6`




# justify-content

* flex-start

  `11` `22` `3333` _ _ _ _ _ _ _ _ _ _ _ _

* flex-end

  _ _ _ _ _ _ _ _ _ _ _ _  `11` `22` `3333` 

* center

  _ _ _ _ _ `11` `22` `3333` _ _ _ _ _ _ _

* space-between

  `11` _ _ _ _ _ _ `22` _ _ _ _ _ _ `3333` 

* space-around

  _ _ `11` _ _ | _ _ `22` _ _ | _ `3333` _



# align-item

* flex-start

  ┍┯┑
  │┿┙
  ││
  ┕┙

* flex-end

  ┍┑
  ││
  │┝┑
  ┕┷┙

* center

  ┍┑
  │┝┑
  │┝┙
  ┕┙

* stretch

  ┍┯┑
  │││
  ┕┷┙

* baseline



# align-self

* 用在於覆寫已經套用 align-items 的屬性



# flex

* `flex-basis`
  * 基本大小
  * 0，依系統分配
  * auto，扣掉原本的長度再拿去分配
* `flex-grow`
  * 如果 Container 有多餘的空間時，分配給 Item 拉長的比例。
* flex-shrink
  * 如果 Container 空間不夠時，分配給 Item 壓縮的比例。


* flex: `flex-grow` `flex-shrink` `flex-basis`
  * 分配的`flex-grow`

