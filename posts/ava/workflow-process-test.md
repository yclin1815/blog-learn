---
title: 測試文章
date: 2023-04-10
author: ava
tags: [Project]
layout: zh-tw/layouts/post.njk
---

![](/img/posts/ava/workflow.process/workflow.process.jpeg)

## 前言：為什麼需要產品開發流程？

<!-- summary -->
面對快速發展的客戶群體與機會，不斷的尋找甜蜜點是身為產品經理的目標之一，而專案經理的目標更是明確，讓這些產品、專案、功能順利交付到使用者的手上，有效解決他們的需求。在這樣的目標之下，必須建立一套產品開發流程，讓產品的運作從構想、設計、開發到交付的過程都能夠通順並如期推出。具體來說，Cymetrics 會把整體流程拆分成以下3個部分：
1. 需求流程
2. 設計流程
3. 開發流程
<!-- summary -->


### 1.需求流程
除了開發自有產品外，Cymetrics也會接一些專案服務（弱點掃描、滲透測試、各方合作等）。不論是這些專案、客戶建議或內部夥伴的回饋，都會需要走這個流程，也是整體流程的第一步。內部透過設置許願池，讓銷售、行銷、產品經理、設計、工程師等遵照規範來提出具體需求。

許願池創立的初衷是希望，不論需求者的角色為何，我們都希望能夠看到具體的需求描述、預期時間以及需求目的，這些重要的資訊是能使專案經理更為有效地去理解並提供相對應的幫助，與此同時間可以降低缺少紀錄、工作到一半被打擾的現象發生。

根據觀察，可以將需求流程分為2個問題分類：許願或需求以及評估。在許願池出現的需求們，會由產品團隊或資安團隊進行討論並給出初步回覆與規劃，如有急件影響到現行開發的順序，則會與相關利益者進行必要的討論。


### 2.設計流程
不論是由許願池獲得的回饋延伸回產品本身或由產品經理自行提出，都會經過以下的設計流程：
1. **[PM Spec]** 去找設計師之前要先將PRD（產品需求文檔）開好（ticket 內含spec 規格, wireframe 線框稿, 產品生命流程等）
2. **[UX Design]** 在設計師著手設計圖前會先開會討論，釐清PM的需求。會議結束後，開始設計wireframe。初版wireframe完成後會再次跟PM開會，確認整體流程的正確性，若不正確則會修改，與開會討論，一直重複修改、開會的流程直至整體都確認無誤，才能進行到下一階段。 ⇒ 此時會輸出初版定稿wireframe設計。
3. **[Wireframe Kickoff]** 有了初版定稿wireframe設計後，會與工程團隊一同討論流程在實作上的可行性、困難度與相關回饋。
4. **[Mockup Design]** Wireframe 確認過後，才會到設計mockup（精美圖）的階段，這塊會以工程師給予的回饋基底下去做更細節的設計。
5. **[Mockup Kickoff 1]** 當mockup設計完後，設計師會再次與PM討論並確認設計圖如PM所想。此時的mockup設計的大原則以不影響流程為主。⇒ 此時輸出暫時版的mockup。
6. **[Usability Test]** 有了暫時版的mockup，就可以開始規劃Usability test（易用性測試）所需要的Prototype（雛形）了。有Prototype能夠協助使用者在進測試時，對目前的設計畫面有更直覺性的體驗與反饋。經過usability test，再進入工程是一種較省開發成本的做法，可以避免開發出使用者體驗不佳或使用者不需要的功能。應用性測試以最少一次測試為基準，必要時或時間充足時可拉至2次的測試，當然也有一些功能不需要進行這個步驟。
7. [**Mockup Kickoff 2]** Usability test完畢會進行最終的mockup設計。 ⇒ 此時輸出最終版的mockup（精美圖）。
8. **[Sprint Grooming]** 最終版的mockup會接著進入Sprint Grooming，針對下個sprint所要實作的spec與畫面進行討論。預期此時如需要調整mockup的話將會是微幅調整。
9. **[Done]** 最終調整完的mockup確認無誤後，會將圖輸出到Zeplin，走完這步就算完成了設計流程，設計師的工作也告一段落了。

### 3.開發流程
設計流程結束後，會按照時程安排進入開發流程，基本上到這一步就算走過一半的產品開發流程了，接下來就交由工程師們實際將產品開發出來。
1. **[Functional Specs]** PM會將之前寫好的PRD補上最終版的mockup。如果該PRD沒有相對應的家（EPIC）時，PM會新增EPIC作為存放PRD的地方，除了PRD之外，也會去確認相關mockup使否在Zeplin上並且有其對照的i18n（語系）。 ⇒ 這時會輸出暫時的PRD, DRD以及i18n。
3.  **[Sprint Grooming]** 準備好的PRD，會跟工程主管以及工程團隊一起開Sprint Grooming。會議最主要就是跟工程師們介紹，下個sprint要做的具體功能，因此PM會把所有的PRD一個一個開出來介紹，並進行討論。 ⇒ 此時輸出最終的PRD（與工程師討論過後的最終版本）。
4. **[Sprint Planning]** 再進入該sprint前，會請工程師根據每個PRD開出task，並且預估完成這張單所需的時數附上。有時候一個sprint不一定能消化所有的任務，因此Sprint Planning扮演著一個很重要的角色，討論實作上的優先順序。
5. **[Dev]** 接著進入為期兩週的sprint開發流程。
6. **[QA/PM Testing]** 工程師開發完、程式碼合併完後，會將成果上到測試環境，此時會由QA/PM做相關測試。QA會去測試環境將PRD及開發成果做比對，如果成果與PRD/DRD不一致則會開bug單請工程師修復。
7. **[Security Testing]** 解決完bug單後，會請資安人員幫忙針對開發成果進行資安測試，以確保即使推進新的或更版的產品，也能保持一貫的安全。
8. **[Done]** 走過以上的所有步驟，才能說開發流程完成，也才能讓使用者接觸到產品本身。

以上三個階段的流程都走完後，我們會去監測並追蹤使用者回饋，然後即時反應到產品設計與規劃上。


## 產品開發流程中常見的挑戰
理想上會希望所有的產品都能安穩地走過上述的每個流程，但現實是不可能，這也是做專案經理最大的考驗，如何好好的處理與降低未知的變化。計劃真的趕不上變化，在實際執行時會因應突如其來的趨勢、資源與現實層面（EX:前一個產品開發的速度不如預期）的考量而做順序上的調整、跳過某些步驟或甚至直接把專案砍掉。這些隕石的出現就會考驗到專案經理對協調資源、排程的靈活應對能力。


## 結論
看完以上的介紹，相信讀者能夠更理解所謂的產品開發週期。一個產品的生成是需要經過規劃、執行、實作、推出到監測的歷程，這些過程當中都需要很多人的投入與心力，每個產品對我們來說都很重要也都很重視，也因如此所有的決定對我們而言都需要經過很多層次的溝通與認同。

## 關於Cymetrics
Cymetrics是一間做資安服務的廠商，除了自有產品的開發外，我們也有在做弱點掃描、滲透測試、特殊專案等服務。我們的觸角延伸到不少產業，類舉製造、電子商務、IC半導體等等都是我們密切合作的對象。海外市場也是我們的目標之一，去年很幸運已經能夠在東南亞擁有合作夥伴，今年當然也會持續擴大這一塊的商務。雖然我不是專業投資人，但這成績聽起來很不錯吧？
歡迎更了解我們：https://cymetrics.io
