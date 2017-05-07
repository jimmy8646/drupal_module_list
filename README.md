## Drupal Module 整理列表
對於新手來說學習 CMS 架站最困難的點就是：玩全不知道有哪些模組可以用，又或是模組的功用為何，與其浪費大量的時間去嘗試模組跟踩雷，不如看看以下模組清單與點評

又有鑑於突然想找模組卻忘記模組名稱，又或是有看到好用的模組卻沒記錄起來這件事情感到可惜，特別開此一篇文章來記錄模組的名稱以及功能，也藉此希望能幫助到新手選擇模組。

## 必裝模組，沒裝不能活
建立好一個新的 Drupal 站有些模組我是必裝的，如果這些模組都沒裝會失去很多強大的功能阿
* [Ctools](https://www.drupal.org/project/ctools) 這...應該不需要解釋了吧，沒裝網站基本上沒什麼事情可以做的
* [Views](https://www.drupal.org/project/views) 同上，製作頁面，區塊都必用
* [Module Filter](https://www.drupal.org/project/module_filter) 優化模組管理介面
* [CKEditor](https://www.drupal.org/project/ckeditor) 所見即所得編輯器，連 Library 都不需要裝，現在直接掛 CDN 了
* [Libraries](https://www.drupal.org/project/libraries) 有需要 Library 的模組都需要這個模組

## Slideshow
介紹用來製作圖片輪播的模組，各有優缺點大家可以自行斟酌。

[Views Slideshow](https://www.drupal.org/project/views_slideshow)   
備註：搭配 views 服用效果也很簡單  
[Flex Slider](https://www.drupal.org/project/flexslider)  
備註：如果是 V1 版本需要另外搭配 [FlexSlider Views Slideshow](https://www.drupal.org/project/flexslider_views_slideshow) V2 之後就已經內建(我很久沒用這個模組了如果有錯也請大家包容)  
[Slick Carousel](https://www.drupal.org/project/slick) (大推)  
備註：目前都使用這套模組，功能強大樣式多樣，擴充性的模組也很多  
[Backstretch](https://www.drupal.org/project/backstretch)  
用途：用來製作背景式全螢幕的圖片輪播居多
備註：使用起來彈性較小，需要搭配 context 一起使用比較好一點

## Layout
介紹用來幫助排版或是版形的模組

[Context](https://www.drupal.org/project/context)  
用途：比起核心的區塊功能更佳的彈性以及強大與大多數的模組整合的非常好  
[Panels](https://www.drupal.org/project/panels)  
用途：可以將內容切成自己想要的 Region 有單欄、兩欄、三欄多種選擇  
備註：搭配 Page Manager 一起服用效果更佳。  
[Quick Tabs](https://www.drupal.org/project/quicktabs)  
用途：可以製作出切換 Tab 的效果，Tab 數量可以無限新增、支援 AJAX 效果，可以選擇預設顯示 Tab 或不顯示
備註：一個 Tab 可以是 node block view callback 運用非常靈活，也是一個很強大的模組

## Block
介紹將輸出結果為 Block 的或是 Block 相關功能的模組

[Block Group](https://www.drupal.org/project/blockgroup)  
用途：為 Drupal Block 產生一層 wrapper，有助於前端工程師撰寫樣式。  
支援 Drupal 版本：Drupal7、Drupal8  
[MultiBlock](https://www.drupal.org/project/multiblock)  
用途：複製網站內已存在的 Block ，使得一個頁面能出現多個一樣的 Block。  
支援 Drupal 版本：Drupal7  
備註：此功能已經加入Drupal8中。  
[Menu block](https://www.drupal.org/project/menu_block)  
用途：將 menu 製做成 block 的好用模組  
[Taxonomy menu block](https://www.drupal.org/project/taxonomy_menu_block)  
用途：將 taxonomy 直接製作成 menu block 的模組，像是 [Menu block](https://www.drupal.org/project/menu_block) 模組與 [Taxonomy menu](https://www.drupal.org/project/taxonomy_menu) 的綜合體  
[Bean](https://www.drupal.org/project/bean)  
用途：有詳細權限控管的 Block 功能，為 Entity 架構支援管理欄位、管理顯示。  
備註：Bean 的 Title 欄位，管理顯示隱藏似乎沒有效果，個人解法就是另外在開一個 title 欄位
[Block Class](https://www.drupal.org/project/block_class)  
用途：可以將 block 新增自己想要的 class


## Field
介紹欄位的模組，細分為三種功能層面來介紹

### Type
介紹產生欄位的種類，通常為新形態的欄位  
[Date](https://www.drupal.org/project/date)  
用途：建立日期欄位，支援彈出日曆工具讓使用者選擇日期。  
備註：如果需要限制日曆的日期需要自己寫 JS code 去限制。  
[Email Field](https://www.drupal.org/project/email)  
用途：此欄位類型會驗證書入的文字是否為 Email 格式。  
[Entity reference](https://www.drupal.org/project/entityreference)  
用途：使 Drupal Entity 之間的資料產生關聯。  
支援 Drupal 版本：Drupal7  
[Serial Field](https://www.drupal.org/project/serial)  
用途：產生流水號的欄位。  
[Computed Field](https://www.drupal.org/project/computed_field)  
用途：用來計算其他欄位的值，將結果儲存於此欄位的模組。  
備註：使用起來並不是很直觀的模組，需要寫一點點小程式於後台。  

### Formatter
[Field Formatter Class](https://www.drupal.org/project/field_formatter_class)  
用途：幫助前端工程師的好用模組～ 針對特定的Field 加上 自訂的 ClassName  
支援 Drupal 版本：Drupal7、Drupal8  
備註：這個模組不支援 ＤＳ的 Field ， 請務必裝此[模組](https://www.drupal.org/sandbox/a65162/2852575)，才能支援 DS 的 Field。  
[Field Permissions](https://www.drupal.org/project/field_permissions)  
用途：針對欄位做特定的權限控管

### Widget
[Entity Reference View Widget](https://www.drupal.org/project/entityreference_view_widget)  
用途：為 Entity Reference 類型的 Field 提供更友善的後台使用介面。  
支援 Drupal 版本：Drupal7  

## Views 相關模組
將會列出與 views 相關性的模組

[Better Exposed Filters](https://www.drupal.org/project/better_exposed_filters)  
用途：將原生的 views exposed 功能進行強化，有多種型態的選擇，如預設的下拉式選單、連結、單選按鈕等，並且有自動提交、支援 AJAX 等功能  
[Better Jump Menus](https://www.drupal.org/project/jump_menu)
用途：比原生 views 的 jump menu 多了層級的概念可以使用。

## 功能增強
將原有的功能增強優化的模組都會在此介紹，可能是使用者體驗、使用者更加便利等

[Administration Views](https://www.drupal.org/project/admin_views)  
用途：將原生幾個無法修改的 views 進行修改使其功能上更加好用，像是原本的"內容"加上 [VBO](https://www.drupal.org/project/views_bulk_operations) 批次處理的功能  
[Adminimal Administration Menu](https://www.drupal.org/project/adminimal_admin_menu)  
用途：將原生上方的 toolbar 加入擴展的功能，支援 RWD 與 [Administration menu](https://www.drupal.org/project/admin_menu) 功能相同
[Administration menu](https://www.drupal.org/project/admin_menu)  
用途：老牌的模組，一樣增強 toolbar 加入擴展的功能  
備註：安裝此模組記得要手動去將原生的 Toolbar 模組關閉，否則兩個 menu 會重疊  
[Back To Top](https://www.drupal.org/project/back_to_top)  
用途：在畫面會出現一個懸浮的按鈕，點擊之後會將畫面捲動至最上方，後台有許多樣式的設定，以及呈現的位置  
[scroll to top](https://www.drupal.org/project/scroll_to_top)  
用途：功能同上，設定的參數並沒有如上述的模組多

## 媒體類
關於圖片，媒體樣式類的模組

[Breakpoints](https://www.drupal.org/project/breakpoints)  
用途：可以用來管理 theme 的 medai query 可以在不同的螢幕大小，將圖片放大或縮小，節省空間

## 社群相關、分享
分享到社群的模組介紹

[AddToAny](https://www.drupal.org/project/addtoany)  
備註：台灣常用的 Line Wechat 他都有提供，也提供客製化 Icon 的功能目前也是用這款(大推)  
[AddThis](https://www.drupal.org/project/addthis)  
備註：提供了基本的一些社群分享的服務，很可惜的是沒有台灣人常用的 Line 而且在 HTTPS 的環境下會有問題

## 購物車
購物車相關的模組介紹

[Drupal Commerce](https://www.drupal.org/project/commerce)  
用途： Drupal 的購物車模組擁有基本的產品、購物車功能、結帳、顧客資訊、手續費等功能  
[Commerce Addressbook](https://www.drupal.org/project/commerce_addressbook)  
用途：在結帳頁填寫客戶資料時，可以讓客戶選擇之前填過的資料  
[Commerce Addressbook Extra](https://www.drupal.org/project/commerce_addressbook_extra)  
用途：上述模組的加強版，可以選擇顯示不同的資訊為 Addressbook 下拉選單的文字，以及是否讓使用者在註冊時就填寫資料，以及啟用與否等  
[Commerce Cart Form Checkout Pane](https://www.drupal.org/project/commerce_cart_form_checkout_pane)  
用途：在結帳頁面時可以將購物車顯示在頁面內，並且有 AJAX 更新購物車的工能  
[Commerce Cart Pane](https://www.drupal.org/project/commerce_cp)  
用途：在購物車頁可以細項的調整 component 的位置以及自帶兩個小模組可以在購物車頁面，選擇貨運方式以及輸入折扣碼  
[Commerce Cart View Override](https://www.drupal.org/project/commerce_cart_view_override)  
用途：可以讓我們改寫原本購物車的 view 也可以改寫路徑，原生路徑為/cart  
[Commerce Checkout Redirect](https://www.drupal.org/project/commerce_checkout_redirect)  
用途：一定要登入才可以購買結帳，讓匿名使用者要結帳時，跳轉至自訂的路徑  
[Commerce Coupon](https://www.drupal.org/project/commerce_coupon)  
用途：讓使用者可以輸入折扣碼獲得折扣的功能，因為完整兼容 [Commerce Discount](https://www.drupal.org/project/commerce_discount) 所以折扣的方式非常的彈性  
[Commerce Currency Settings](https://www.drupal.org/project/commerce_currency_settings)  
用途：可以自訂貨幣的顯示方式，也可以 callback 自己寫 code 顯示方式或是轉換比率，也可以藉此達到去除小數點的功能  
[Commerce Discount](https://www.drupal.org/project/commerce_discount)  
用途：購物的折價方式，可以達到免運費、打折、固定的折扣、貨運方式升級、買a送b等，可以滿足大部分的商業需求  
[Commerce Discount Extra](https://www.drupal.org/project/commerce_discount_extra)  
用途：功能同上，提供更多的折扣方式如買三送二、各個商品各自打折  
[Commerce Extra](https://www.drupal.org/project/commerce_extra)  
用途：購物車的功能強化，有結帳頁面提供登入功能、購物車提供按鈕增減數量、顧客資料預先填入等等  
[Commerce Responsive UI](https://www.drupal.org/project/commerce_responsive_ui)  
用途：此模組改寫掉了很多購物車頁面的 template 方便開發者撰寫樣式，像是原生的 checkout review 頁面原本都是表格，就被模組改寫掉了  
[Commerce Fancy Attributes](https://www.drupal.org/project/commerce_fancy_attributes)  
用途：如果模組有顏色的屬性可以使用這個模組，將顏色顯示出來，可是必須要自己填入色碼
