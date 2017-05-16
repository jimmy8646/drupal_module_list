## Drupal Module 整理列表
對於新手來說學習 CMS 架站最困難的點就是：如何挑選模組，以及模組的功用為何，連選擇模組都是一門學問，自己摸索又會浪費大量的時間在踩雷上，不如看看以下整理出來的模組清單，以下這些模組都是個人使用過所整理出來的，個人常使用的模組也會推薦給大家。

又有鑑於突然想找模組卻又忘記模組名稱，又或是有看到好用的模組卻沒記錄起來這件事情感到可惜，特別開此一篇文章來記錄模組的名稱以及功能，希望能幫助到學習 Drupal 的新手，也藉由此機會整理模組。

本文的介紹方式將會以 基本模組-區塊-資料架構-資料呈現-排版-權限-功能增強 這樣的大方向來進行模組分類，也可以點下方的索引找到你想看的類型。

* [個人必裝的模組](#base)
* [區塊 (Block)](#block)
* [欄位 (Field)](#field)
* [Views 相關模組](#views)
* [圖片輪播 (Slideshow)](#slideshow)
* [排序 (Sort)](sort)
* [Layout 相關](#layout)
* [選單 (Menu) 類模組](#menu)
* [權限 (Permission) 類模組](#permission)
* [功能增強](#power)
* [媒體 (Media) 類](#media)
* [使用者 (User) 相關](#user)
* [社群相關、分享](#social)
* [購物車](#commerce)
* [開發類](#dev)

<h2 id="base">個人必裝的模組</h2>
建立好一個新的 Drupal 站有些模組是必裝的，很多強大的模組都是基於這些模組所開發出來的，這些模組也可以算是核心模組了吧，甚至有些是 Drupal8 也直接納入核心功能。

* [Ctools](https://www.drupal.org/project/ctools) 看他的使用量就知道他是必裝的模組，他提供了很多個 API 功能讓使用者開發更方便。
* [Views](https://www.drupal.org/project/views) 直接使用介面來對資料庫撈取資料，只要對 Views 撈資料夠熟悉就能夠解決百分之八十的問題。
* [Module Filter](https://www.drupal.org/project/module_filter) 這個模組直接將我們的模組列表頁面改寫，將模組群組化，搜尋上更加的方便，也讓模組的資訊更加的詳細。
* [CKEditor](https://www.drupal.org/project/ckeditor) 提供使用者在文字區塊時出現類似 Word 工具列的功能讓使用者發表文章更加方便。
* [Libraries](https://www.drupal.org/project/libraries) 有需要 Library 的模組都會需要這個模組的 API 所以也是必裝的。


<h2 id="blcok">區塊 (Block)</h2>
Block 為 Drupal 的功能之一，區塊的好處在於可以到處重複使用，壞處就是權限的控管並沒有很詳細的處理而且他不是 Entity 的架構，整個網站的組成不外乎區塊跟頁面，所以區塊相關的模組特別整理出來一塊。

[Bean](https://www.drupal.org/project/bean) (大推)  
用途：就像我上面敘述提到的，原生的 Block 缺乏權限的控管，以及不是 Entity 的架構，而這個模組正好解決此問題，有詳細的權限控管以及、管理欄位、管理顯示非常好用。  
備註：Bean 的 Title 欄位，管理顯示隱藏似乎沒有效果，個人解法就是另外在開一個 title 欄位。  
[Menu block](https://www.drupal.org/project/menu_block)  
用途：將 menu 直接製做成 block 的好用模組，如果 menu 為多階層，可以設定層級相關的功能。  
[Block Group](https://www.drupal.org/project/blockgroup)  
用途：提供將區塊群組的功能，類似於 Region 而前台會產生一層 wrapper，有助於前端工程師撰寫樣式，如果有許多個區塊需要包在一起可以考慮使用這個模組。  
支援 Drupal 版本：Drupal7、Drupal8  
[Taxonomy menu block](https://www.drupal.org/project/taxonomy_menu_block)  
用途：將分類直接製作成 menu block 的模組，省去了 [Menu block](https://www.drupal.org/project/menu_block) 與 [Taxonomy menu](https://www.drupal.org/project/taxonomy_menu) 的模組整合，有時想簡單的呈現分類選單，可以使用這個模組，當然不會比前兩者組合來的彈性。  
[MultiBlock](https://www.drupal.org/project/multiblock)  
用途：複製網站內已存在的 Block ，使得一個頁面能出現多個一樣的 Block。  
支援 Drupal 版本：Drupal7  
備註：此功能已經加入Drupal8中。  
[Block Class](https://www.drupal.org/project/block_class)  
用途：可以將 block 新增自己想要的 class，方便撰寫前台樣式。  
[Floating block](https://www.drupal.org/project/floating_block)  
用途：將區塊位子(css position:fixed)在畫面上的狀態。  


<h2 id="field">欄位 (Field)</h2>
整個 Drupal 站好不好用取決於 欄位建的好不好，使用者用起來會不會覺得麻煩都是要考慮的因素，當然也有很多模組，不管是資料的形態、顯示的方式、欄位的工具等等，這些模組真的是太多了所以我將會列出我有用過的模組。

### 欄位類型 (Field type)
某方面來講建立欄位就是在定義資料庫的形態，所以為了滿組使用者龐大的需求，欄位的類型自然不少，介紹一些新類型的欄位。

[Entity reference](https://www.drupal.org/project/entityreference)  
用途：使 Drupal Entity 之間的資料產生關聯，簡單的來說就是資料之間的橋梁透過 Entity reference 可以從 A Type 找到 B type 只要有關聯就一定有辦法撈出資料。  
支援 Drupal 版本：Drupal7  
[Link](https://www.drupal.org/project/link)  
用途：專門存放 URL 的欄位，並且可以選擇顯示的方式，不管是顯示網址、還是顯示 Title 是否開新視窗等，只要跟連結有關的設定他都有提供。  
[Date](https://www.drupal.org/project/date)  
用途：建立日期欄位，支援彈出日曆工具讓使用者選擇日期。  
備註：如果需要限制日曆的日期需要自己寫 JS code 去限制或是使用 [Date Restrictions](https://www.drupal.org/project/date_restrictions)。  
[Date Restrictions](https://www.drupal.org/project/date_restrictions)  
用途：搭配 [Date](https://www.drupal.org/project/date) 一起使用可以限制日期，是不用寫 JS 的方法，模組自帶其他擴充模組有更細部的設定。
備註：此模組的設定是欄位共通的，只要是共用欄位都會遭到模組的限制。  
[Email Field](https://www.drupal.org/project/email)  
用途：此欄位類型會驗證輸入的文字是否為 Email 格式。  
[Serial Field](https://www.drupal.org/project/serial)  
用途：產生流水號的欄位。  
[Computed Field](https://www.drupal.org/project/computed_field)  
用途：用來計算其他欄位的值，將結果儲存於此欄位的模組。  
備註：使用起來並不是很直觀的模組，需要寫一點點小程式於後台。  

### 欄位顯示 (Formatter)
既然我們有了資料，接著就要討論將欄位顯示出來的**樣式**，不管是加 class ，還是資料的呈現方式都有許多模組，列出幾個比較常用的模組。

[Field Group](https://www.drupal.org/project/field_group) (大推)  
用途：可用在管理欄位、管理顯示，可以新增 group 欄位將欄位群組起來，並且顯示為 Fieldset、Tab 又或是可以用 HTML 產生 Wrapper ，很多很多功能。  
[Image Link Formatter](https://www.drupal.org/project/image_link_formatter)  
用途：為圖片欄位的顯示方式，可以選擇要使用哪個欄位，將圖片變成有連結功能，不需要在用 views 去改寫設定，非常好用。  
[Smart Trim](https://www.drupal.org/project/smart_trim)  
用途：核心的擷取字數功能比較簡單並無太多的客製化設定，此模組擷取功能較為彈性。  
[Field Formatter Class](https://www.drupal.org/project/field_formatter_class)  
用途：幫助前端工程師的好用模組～ 針對特定的Field 加上 自訂的 ClassName  
支援 Drupal 版本：Drupal7、Drupal8  
備註：這個模組不支援 DS 的 Field ， 請務必裝此[模組](https://www.drupal.org/sandbox/a65162/2852575)，才能支援 DS 的 Field。  


### 欄位介面工具 (Widget)
雖然是說核心的模組就已經可以滿足大部分的需求，可是總是會覺得差那麼一點點，或是阿~這裡在多幾個功能就更好的感覺，所以列出幾個改變選取資料介面的模組。

[Inline Entity Form](https://www.drupal.org/project/inline_entity_form)  
用途：如果欄位為 Entity Reference 類型，使用 Inline Entity Form 可以直接在當前頁面編輯、新增、複製被 Reference 的 Entity  
[Entity connect](https://www.drupal.org/project/entityconnect)  
用途：允許被 Entity References 的資料直接使用此模組新增、編輯，省去很多切換頁面的時間  
[Entity Reference View Widget](https://www.drupal.org/project/entityreference_view_widget)  
用途：為 Entity Reference 類型的 Field 提供更友善的後台使用介面。  
支援 Drupal 版本：Drupal7  


### 功能
剩下功能層面的模組歸類在這裡。

[Display Suite](https://www.drupal.org/project/ds)  
用途：將欄位的功能更加細分出來，不只管理欄位、管理顯示也可使用，功能非常強大，可以自行新增 code 欄位，也可以新增 view mode 非常好用的模組。  
[Field Permissions](https://www.drupal.org/project/field_permissions)  
用途：針對欄位做權限控管，可以針對至角色檢視、編輯的權限  
[Field validation](https://www.drupal.org/project/field_validation)  
用途：可以對欄位輸入的資料進行驗證，提供正則表達式，以及多種驗證方式  


<h2 id="views">Views 相關模組</h2>
當我們有了資料欄位，接著就可以開始考慮資料的輸出方式，在此列出幾個 Views 個人覺得還不錯的相關模組。

[Better Exposed Filters](https://www.drupal.org/project/better_exposed_filters)  
用途：將原生的 Views Exposed 功能進行強化，有多種型態的選擇，如預設的下拉式選單、連結、單選按鈕等篩選的方式，並且有自動提交、支援 AJAX 等功能。  
[Better Jump Menus](https://www.drupal.org/project/jump_menu)  
用途：比原生 Views 的 Jump menu 多了層級的概念可以使用。  
[FooTable](https://www.drupal.org/project/footable)  
用途：為 Views 的一種格式，可以將輸出的 Table 於不同的螢幕大小將欄位，並且提供收展的功能。  
[Taxonomy Views Integrator](https://www.drupal.org/project/tvi)  
用途：用 Views 改寫路徑 `taxonomy/trem/%` 可以使用此模組將不同的分類頁改寫，並且分類有繼承的概念。  
備註：要開啟權限才能在分類看到設定選項。  
[Views Accordion](https://www.drupal.org/project/views_accordion)  
用途：用 Views 作出類似手風琴可以開合的效果。  
[Views Conditional](https://www.drupal.org/project/views_conditional)  
用途：在 Views 內可以根據不同的條件顯示不同的欄位。  


<h2 id="slideshow">圖片輪播 (Slideshow)</h2>
正所謂有圖先贏一半，圖片漂亮在贏一半，只要網站有一個美美 Slideshow 看起來就是不一樣，同時也可以幫助網站 promote 內容的好幫手，在此列出了一些常用的模組，以下這幾個各有優缺大家可以自行斟酌選擇自己想要的模組來使用即可。

[Slick Carousel](https://www.drupal.org/project/slick) (大推)  
備註：目前都使用這套，功能強大樣式多樣，擴充性的模組也很多，不管你是同時顯示三個還是五個，後台都可以進行設定。  
[Flex Slider](https://www.drupal.org/project/flexslider)  
備註：如果是 V1 版本需要另外搭配 [FlexSlider Views Slideshow](https://www.drupal.org/project/flexslider_views_slideshow) 使用起來與 Views Slideshow 沒什麼差別，對於行動裝置較為友善，使用手指拖曳就可以切換上下張，設定也比 Views Slideshow 多一點。  
[Views Slideshow](https://www.drupal.org/project/views_slideshow)   
備註：最基本款的圖片輪播功能，如果沒有特殊的需求使用這款即可。  
[Backstretch](https://www.drupal.org/project/backstretch)  
用途：用來製作背景式全螢幕輪播。  
備註：如果你的網站首頁有全屏大圖輪播可以推薦使用這個，使用起來沒有太多可以設定的地方，只要搭配 context 一起使用就可以看到效果。  

<h2 id="sort">排序 (Sort)</h2>
介紹可以讓使用者單獨拉出想要的資料並且自定排序的模組。

[DraggableViews](https://www.drupal.org/project/draggableviews)  
用途：用 views 製作出一個可以拖曳排序的功能。  
備註：建議新增一個數字欄位讓模組進行排序，在以此欄位當做排序的依據。  
[Entityqueue](https://www.drupal.org/project/entityqueue)  
用途：與 [Nodequeue](https://www.drupal.org/project/nodequeue) 相同功能的模組，只是此模組可以對應到任何 Entity 的結構  
[Nodequeue](https://www.drupal.org/project/nodequeue)  
用途：針對內容類型的內容可以自行排序  
[Flag](https://www.drupal.org/project/flag)  
用途：可以用來特別標記 Entity  

<h2 id="layout">Layout 相關</h2>
原生的區塊功能如果要拿來排版其實只能針對路徑來做判斷，條件稍為簡單了一點，所以介紹幾個幫助排版或是切版形的模組，用了這些模組之後排版就可以更加的彈性。

[Context](https://www.drupal.org/project/context)  
用途：比起核心的區塊功能更佳的彈性以及強大與大多數的模組整合的非常好  
[Panels](https://www.drupal.org/project/panels)  
用途：可以將內容切成自己想要的 Region 有單欄、兩欄、三欄多種選擇  
備註：搭配 Page Manager 一起服用效果更佳。  
[Quick Tabs](https://www.drupal.org/project/quicktabs)  
用途：可以製作出切換 Tab 的效果，Tab 數量可以無限新增、支援 AJAX 效果，可以選擇預設顯示 Tab 或不顯示
備註：一個 Tab 可以是 node block view callback 運用非常靈活，也是一個很強大的模組  

<h2 id="menu">選單 (Menu) 類模組</h2>
當我們有了畫面有了資料之後就可以開始選擇 Menu 相關的模組將連結掛上。

[Adminimal Administration Menu](https://www.drupal.org/project/adminimal_admin_menu)  
用途：將原生上方的 Toolbar 加入 dropdown 的功能，同時支援 RWD 與 [Administration menu](https://www.drupal.org/project/admin_menu) 功能相同。  
[Menu Editor](https://www.drupal.org/project/menu_editor)  
用途：一次可以編輯大量連結的方便模組。  
[Menu position](https://www.drupal.org/project/menu_position)  
用途：在 Node 頁時將 Menu 亮燈(active)的模組，可自定路徑。  
[Menu HTML](https://www.drupal.org/project/menu_html)  
用途：可以直接在 Menu 輸入 HTML。  
[Menu token](https://www.drupal.org/project/menu_token)  
用途：在建立 Menu 可以使用 Token。  
[Menu Badges](https://www.drupal.org/project/menu_badges)  
用途：類似 FB 通知的功能，可以顯示數字在連結旁，通常用於購物車以及收件夾等功能。  
[Administration menu](https://www.drupal.org/project/admin_menu)  
用途：老牌的模組，一樣增強 Toolbar 加入 dropdown 的功能  
備註：安裝此模組記得要手動去將原生的 Toolbar 模組關閉，否則兩個 Menu 會重疊。  
[Responsive Menus](https://www.drupal.org/project/responsive_menus)  
用途：於設定的寬度之下自動將選單變成 RWD menu 後台可設定多種樣式，懶人福音  
[Taxonomy Menu Trails](https://www.drupal.org/project/taxonomy_menu_trails)  
用途：在分類頁時將 menu 亮燈(active)的模組，可自定路徑。  


<h2 id="permission">權限 (Permission) 類模組</h2>
將會列出一些權限的模組

[Filter permissions](https://www.drupal.org/project/filter_perms)  
用途：將核心的權限頁面加入篩選的功能  
[Fast Permissions Administration](https://www.drupal.org/project/fpa)  
用途：一樣是將核心的權限頁面加入篩選的功能只是這個模組的篩選是針對角色  
[Masquerade](https://www.drupal.org/project/masquerade)  
用途：使用此模組可以直接切換至他人的帳號方便檢查權限設定是否正確  
[Override node options](https://www.drupal.org/project/override_node_options)  
用途：原生的 Node option 權限控管並沒有很詳細，此模組可直接改寫 Node option 的權限，例如單獨只開啟發佈選項的權限等。  
[Taxonomy access fix](https://www.drupal.org/project/taxonomy_access_fix)  
用途：管理分類的權限並沒有新增的權限，此模組讓允許其他角色新增分類。  
[Publish Content](https://www.drupal.org/project/publishcontent)  
用途：好用的上下架模組，提供一個連結可以將內容上架、下架  
[view_unpublished](https://www.drupal.org/project/view_unpublished)  
用途：其他角色可以看見未發表文章的權限，原生權限沒有效果。  
[Tab Tamer](https://www.drupal.org/project/tabtamer)  
用途：可以隱藏許多系統內建的 Tab。  
備註：如果記憶體不足會無法顯示出全部的 Tab ，有時也會有無法儲存設定的 BUG。  


<h2 id="power">功能增強</h2>
將原有的功能增強優化的模組都會在此介紹，可能是使用者體驗、使用者更加便利等。

[Administration Views](https://www.drupal.org/project/admin_views)  
用途：將原生幾個無法修改的 views 進行修改使其功能上更加好用，像是原本的"內容"加上 [VBO](https://www.drupal.org/project/views_bulk_operations) 批次處理的功能  
[Back To Top](https://www.drupal.org/project/back_to_top)  
用途：在畫面會出現一個懸浮的按鈕，點擊之後會將畫面捲動至最上方，後台有許多樣式的設定，以及呈現的位置  
[scroll to top](https://www.drupal.org/project/scroll_to_top)  
用途：功能同上，設定的參數並沒有如上述的模組多  
[Entity menu links](https://www.drupal.org/project/entity_menu_links)  
用途：將核心的 menu 透過 [UUID](https://www.drupal.org/project/uuid) 的方式將 menu 轉成類似 Entity 的架構  
備註：此模組並不會更動到任何架構，可是你可以在 Views 發現有 Menu 可以撈出來使用  
[Font Awesome Icons](https://www.drupal.org/project/fontawesome)  
用途：輸入特別的 HTML 以及 class 就可以變成文字 icon  
[Inline Entity Form Table View Mode](https://www.drupal.org/project/ief_table_view_mode)  
用途：將 Inline Entity Form 的顯示表格可以自訂顯示方式  
[Page Preview](https://www.drupal.org/project/pagepreview)  
用途：原生的預覽功能在顯示出文章上會有一點問題，此模組預覽功能較能看到正確的顯示內容  
[Workbench](https://www.drupal.org/project/workbench)  
用途：可以製作出我的工作室的功能，類似於主控台。  


<h2 id="media">媒體 (Media) 類</h2>
關於圖片，媒體樣式類的模組

[Media](https://www.drupal.org/project/media)  
用途：提供類似檔案總管的功能，讓使用者上傳圖片、檔案、影片等功能，非常強大的一個模組。  
[Media CKEditor](https://www.drupal.org/project/media_ckeditor)  
用途：讓使用者在 CKEditor 使用 Media 上傳圖片算是整合兩者的模組  
[Manual Crop](https://www.drupal.org/project/manualcrop)  
用途：讓使用者可以自行裁切圖片想要的區域，對於不會做圖的使用者大力推薦  
[File Field Sources](https://www.drupal.org/project/filefield_sources)  
用途：上傳檔案時可以直接輸入 URL 、選擇已經上傳過的檔案等  
[FileField Sources Plupload](https://www.drupal.org/project/filefield_sources_plupload)  
用途：整合 [Plupload](https://www.drupal.org/project/plupload) 可以一次大量上傳檔案  
[Plupload integration](https://www.drupal.org/project/plupload)  
用途：與多數模組整合的批次上傳的模組  


<h2 id="user">使用者 (User) 相關</h2>
使用者相關的模組，不管是註冊相關還是使用者功能的模組都會列在此分類。

[profile2](https://www.drupal.org/project/profile2)  
用途：可以新增與使用者相關連的資料類型，例如履歷表個人檔案。  
[Real Name](https://www.drupal.org/project/realname)  
用途：將使用者顯示帳號的地方都可以換成 Real Name ex: 您好，王大明  
備註：安裝此模組之後系統會提示你要將註冊的 mail template 更改為 Real Name  
[Email Registration](https://www.drupal.org/project/email_registration)  
用途：允許使用者註冊時使用 Email 註冊，並且使用 Email 作為帳號登入  
[Password Separate Form](https://www.drupal.org/project/change_pwd_page)  
用途：可以將重設密碼頁面獨立出來，滿足設計的需求。  


<h2 id="social">社群相關、分享</h2>
分享到社群的模組介紹

[AddToAny](https://www.drupal.org/project/addtoany)  
備註：台灣常用的 Line Wechat 他都有提供，也提供客製化 Icon 的功能目前也是用這款(大推)  
[AddThis](https://www.drupal.org/project/addthis)  
備註：提供了基本的一些社群分享的服務，很可惜的是沒有台灣人常用的 Line 而且在 HTTPS 的環境下會有問題  
[Facebook Comments Block](https://www.drupal.org/project/facebook_comments_block)  
用途：讓網站下方可以出現 FB 留言的功能，可以調整顏色以及留言排序  
備註：需要 FB APP ID  
[Facebook Comments Social Plugin](https://www.drupal.org/project/facebook_comments)  
用途：同上，只是沒有語言設定  
備註：需要 FB APP ID  


<h2 id="commerce">購物車</h2>
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


<h2 id="dev">開發類</h2>
協助開發用的模組，或是不知道該如何分類的模組我都會歸類於此

### Feature 化模組
介紹可以讓網站 Feature 化或是協助 Feature 化的工具

[Feature](https://www.drupal.org/project/features)  
用途：將網站的資料庫設定匯出打包變成模組，可以直接啟用匯出的模組網站就會有打包起來的功能  
[Features Extra](https://www.drupal.org/project/features_extra)  
用途：可以打包原本無法打包的 Nodequeue 以及 Block 還有日期格式  
[Diff](https://www.drupal.org/project/diff)  
用途：網站 Feature 化後，可以用此模組來看哪邊設定被覆寫  
[Strongarm](https://www.drupal.org/project/strongarm)  
用途：可以將網站內的所有 [Variable](https://www.drupal.org/project/variable) 打包起來  


### SEO
關於 SEO 的模組介紹

[Metatag](https://www.drupal.org/project/metatag)  
用途：用於設定 SEO 的模組，還有許多擴展性的模組功能非常強大  
[Imagecache Token](https://www.drupal.org/project/imagecache_token)  
用途：可以在 Token 當中抓取到圖片樣式大小的圖片，安裝  [Metatag](https://www.drupal.org/project/metatag) 時系統會建議你裝此模組  
[Path Breadcrumbs](https://www.drupal.org/project/path_breadcrumbs)  
用途：可以針對動態路徑產生麵包屑，還提供了 Microdata 以及 RDFa 的選項對於 SEO 搜尋結果有很大的幫助  
[Google Analytics](https://www.drupal.org/project/google_analytics)  
用途：埋入 GA 追蹤碼的模組  
[Google Analytics Reports](https://www.drupal.org/project/google_analytics_reports)  
用途：於網站後台直接顯示 GA 的報告  
[Pathauto](https://www.drupal.org/project/pathauto)  
用途：自定意網址路徑的功能  


### 其他
其他開發類別的模組

[CSS Injector](https://www.drupal.org/project/css_injector)  
用途：直接在網站上寫 css  
備註：伺服器上的資料夾權限需要設定才有辦法寫入  
[Devel](https://www.drupal.org/project/devel)  
用途：協助工程師開發時的 debug 工具，或是使用自帶的擴充模組產生假內容，也可直接執行 PHP code  
[Entity Construction Kit (ECK)](https://www.drupal.org/project/eck)  
用途：可以自行建立 Entity 架構的模組，並且不會產生內頁  
[PHPMailer](https://www.drupal.org/project/phpmailer)  
用途：用來讓網站寄信的模組，功能簡單。  
備註：需要安裝 Library 以及要有 SMTP Server  
[Rename Locked Fields](https://www.drupal.org/project/rflocked)  
用途：可以重新命名無法更改的欄位  
[Rules](https://www.drupal.org/project/rules)  
用途：處發事件之後執行客製的動作，功能靈活可是設定稍為複雜  
[Variable](https://www.drupal.org/project/variable)  
用途：提供了一個介面來管理網站的 Variable，也提供了 API 讓我們撰寫模組產生 Variable。  
[Tracking Code](https://www.drupal.org/project/tracking_code)  
用途：埋入追蹤碼的模組。  
