# Flux

* 代替MVC

* one-way data flow 的`概念`

  * 點擊`View` 時，發出一個 `Action`到`Dispatcher`
  * `Dispatcher` 根據 `Action`來更改`Store` 的資料
  * `View` 根據`Store` 的內容更新畫面

* 實作上，有許多第三方的lib

* `Dispatcher` → `Store`

  ​          ↑                      ↓

  ​     `Action`    ←  `View`

  * `Dispatcher`  event system
    * broadcast events
    * registers callbacks
  * `Store`  Store contains Models
  * `View` ui
  * `Action`  touch event



# Redux

* 基於flux

* `Reducer` → `Store`

  ​          ↑                      ↓

  ​     `Action`    ←  `View`

* ​



# react-redux

* 结合Redux 和 React 
* ​