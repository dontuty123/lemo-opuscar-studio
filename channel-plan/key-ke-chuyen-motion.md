# Kể bi kịch bằng chuyển động có nghĩa

Bí quyết lớn nhất khi kể chuyện lịch sử bằng motion graphics làm hoàn toàn bằng code là: **mỗi chuyển động phải mang một ý của câu chuyện, và lời dẫn đã thu là thứ đặt nhịp cho mọi thứ**. Các studio kể chuyện giỏi (Giant Ant, Kurzgesagt, Liz Blazer) đều nói câu chuyện và ẩn dụ hình đi trước, phong cách đi sau. Họ cũng nói cảm xúc đến từ cả một gói gồm kịch bản, giọng, nhịp, âm thanh và nhạc, chứ không từ độ bóng bẩy của hình. Với đề tài thảm họa, công cụ có bằng chứng mạnh nhất là **hệ hình người đếm được** theo truyền thống Isotype. Neil Halloran dùng nó trong "The Fallen of World War II", mỗi hình bằng 1.000 người, và phim đạt hơn 4 triệu lượt xem. Đi kèm là **cú lộ tỉ lệ luôn có một hình người làm mốc**, và **chuyển cảnh liền mạch** dùng làm chất nối mang chủ đề. Người dẫn chuyện biết diễn vẫn làm được trong motion graphics, không cần video AI. Cách làm là ghép năm thứ: thân dựng từ khối đơn giản tách lớp; quay đầu bằng 5 tư thế nội suy; tay bằng IK hai xương hoặc ống cong kiểu RubberHose; mặt bằng các lớp mày, mắt, miệng có thể thay hình; và khớp môi lấy từ Rhubarb hoặc từ mốc thời gian của TTS. Muốn nhân vật "sống", nó không bao giờ đứng yên hẳn (moving hold, thở, chớp), và diễn bằng phản ứng nhiều hơn bằng cử động. Về khung code, chọn Remotion nếu muốn agent viết và render tự động (miễn phí cho cá nhân hoặc nhóm tối đa 3 người). Chọn Motion Canvas nếu muốn kéo mốc nhịp theo lời đọc trên giao diện. Còn kiểu trang `render(t)` của Lemo-Opuscar thì hợp nếu bạn đã quen. Lưu ý an toàn: trang `rainboxlab.org` (nơi từng phát hành Duik) **hiện chuyển hướng sang một tên miền lạ**, không mở link đó.

> **Cách đọc con số.** Con số có link ngay sau là **có nguồn** (ghi rõ nếu nguồn chỉ là blog, bên thứ ba hoặc dành cho giao diện app chứ không cho phim). Con số đánh dấu **(KN)** là kinh nghiệm hoặc suy luận của người tổng hợp, chưa có nguồn đo. Hãy coi chúng là điểm xuất phát, xem bằng mắt rồi chỉnh. Bảng ở cuối báo cáo tách riêng hai loại.
>
> **Thay đổi so với báo cáo trước.** Báo cáo "Bí quyết video hoạt hình kể chuyện" đề xuất chia hai nhánh: Seedance cho người dẫn diễn, code cho phần thông tin. Theo yêu cầu mới của bạn, báo cáo này **bỏ nhánh video AI**. Mọi thứ, kể cả diễn xuất của người dẫn, đều làm bằng motion render bằng code. Phần kịch bản, âm thanh và kênh của báo cáo trước vẫn đúng, nên được dùng lại ở đây khi cần.

## Mỗi chuyển động phải trả lời "nó kể gì", nếu không thì bỏ

Các nguồn đọc được đều đặt câu chuyện lên trước phong cách. Jay Grandin của Giant Ant nói thiết kế đẹp chỉ làm dự án "ngọt" hơn, còn **"if there is no real story, there's no soul"** ([Working Not Working](https://magazine.workingnotworking.com/magazine/2019/7/24/giant-ant)). Tuyên ngôn của studio này phê phán những sản phẩm "beautiful, flawlessly-made" mà "leaves us feeling nothing because it's missing a core idea". Họ kể rằng thời đầu, giới hạn kỹ thuật "forced us not to pass off style as substance", tức là buộc họ không được lấy phong cách thay cho nội dung. Họ liệt kê **bối cảnh, câu chuyện, kịch bản, giọng, nhịp, sound design và nhạc** là những thứ quan trọng ngang nhau trong việc tạo cảm xúc ([Motionographer](https://motionographer.com/2017/01/02/the-ethos-of-giant-ant/)). Ví dụ là trailer liên hoan phim DOXA: hình rất tối giản, nhưng dựng được hồi hộp nhờ âm thanh và nhịp chậm dẫn tới một cú lộ diện ([Motion Array](https://motionarray.com/blog/industry-spotlight-giant-ant)). Với một người làm một mình bằng code, đây là tin tốt. Hình tối giản không phải điểm yếu, nếu nhịp và âm thanh làm đúng việc.

Liz Blazer, tác giả sách "Animated Storytelling", nói **"with animation you can create the rules"**. Hoạt hình tự đặt luật cho thế giới của nó, và mọi công cụ, mọi hiệu ứng phải được hỏi lại xem có phục vụ truyện không ([Motionographer](https://motionographer.com/2016/01/18/tidying-up-for-the-muse-interview-with-liz-blazer-author-of-animated-storytelling/)). Sách của bà có hẳn chương "Designing the Rules" ([O'Reilly](https://oreilly.com/library/view/animated-storytelling-2nd/9780135668023)). Với kênh của bạn, câu này nghĩa là phải viết ra một **"ngữ pháp chuyển động" của kênh** trước khi làm tập đầu. Ví dụ **(KN)**: con tàu luôn chạy từ trái sang phải; người sống là hình màu kem, người mất chuyển sang xám và rơi khỏi hàng; dữ kiện luôn vào màn hình từ dưới lên; ký ức thì mờ dần, hiện tại thì cắt gọn. Khi luật đã viết ra, người xem học được luật sau vài phút, và từ đó mỗi lần luật bị phá đều mang nghĩa. Bài học từ thiết kế giao diện cũng dùng được: **mỗi chuyển động phải có một nhiệm vụ nói được trong một câu**; nếu không giúp người xem hiểu thì bỏ ([Clay](https://clay.global/blog/web-design-guide/motion-design-principles)). Báo cáo trước cũng có một cảnh báo cùng hướng: zoom, chữ, tiếng đập và lớp phủ liên tục "can create activity without meaning", tức là tạo cảm giác bận rộn mà không có ý nghĩa ([CapCut/Dreamina](https://dreamina.capcut.com/ai-video/youtube-audience-retention)).

Kurzgesagt cho thấy quy trình biến ý thành hình. Họ viết **khoảng một chục bản nháp kịch bản**, phác **"visual metaphors for each scene"** (một ẩn dụ hình cho mỗi cảnh) trước khi minh họa, và để **giọng đọc của Steve quyết định timing** cho đội animation. Nhạc được sáng tác riêng cho từng video ([Kurzgesagt](https://kurzgesagt.org/youtube/)). Một video của họ tốn khoảng 1.200 giờ công ([VoiceTube](https://voicetube.com/videos/123700), nguồn trung gian). Phim "Metamorphosis" của Buck đi thêm một bước: nhịp chuyển động bám theo nhịp văn của Hunter S. Thompson, thành một "visual onslaught" (cơn lũ hình ảnh) ([Motionographer](https://motionographer.com/2012/03/26/interview-buck-good-books-metamorphosis/)). Nghĩa là chuyển động có thể mang chính giọng văn của người kể. Lời văn dồn dập thì hình dồn dập; lời văn chậm và trang nghiêm thì hình cũng chậm. Không có nguồn chuẩn nào dùng đúng cụm "motion with meaning" làm một luật có tên. Đây là một tinh thần chung của nghề, nhưng là tinh thần mà mọi nguồn đều chia sẻ.

## Con số bi kịch phải đếm được và luôn có một con người đứng cạnh

Với thảm họa, câu hỏi khó nhất là làm sao cho người xem *cảm* được một con số lớn. Luật đầu tiên của Isotype (Otto Neurath) trả lời: **lượng lớn hơn không vẽ bằng hình to hơn, mà bằng nhiều hình cùng cỡ hơn, mỗi hình mang một giá trị cố định**, nên người xem đếm được ([Wikipedia: Isotype](https://en.wikipedia.org/wiki/Isotype_(picture_language))). Isotype cũng dùng được để kể chuyện theo thời gian. Ví dụ "Home and Factory Weaving in England" dùng một hình cho 10.000 công nhân ([eagereyes](https://eagereyes.org/techniques/isotype)). Cần chọn tỉ lệ cẩn thận. Trong ca 128 gia đình ở Bilston năm 1946, nếu một hình bằng 100 gia đình thì vẽ 1 hình sẽ **thiếu khoảng 21,9%**, còn vẽ 2 hình sẽ **dư khoảng 56,2%** ([Visible Language, uc.edu](https://journals.uc.edu/index.php/vl/article/download/5935/4799/7612), chỉ có đoạn trích). Bài học **(KN)**: chọn tỉ lệ sao cho mọi nhóm bạn so sánh đều ra số hình gần nguyên, hoặc cho phép một hình bị cắt dở và nói rõ trong lời dẫn.

Neil Halloran biến luật này thành điện ảnh. Trong "The Fallen of World War II" (khoảng 15 phút), ông cho rằng cột biểu đồ trơn quá trừu tượng, nên xếp cột bằng hình người, **mỗi hình bằng 1.000 người**, để cột trông "to và nặng". Hình lính còn đeo một khẩu súng nhỏ trên vai. Halloran tự viết, đạo diễn, lập trình và đọc lời; Andy Dollerson làm nhạc và âm thanh. Phim có **hơn 4 triệu lượt xem** ([We Are The Mighty](https://www.wearethemighty.com/articles/fallen-io-ww2-fatalities-video)). Phim chia ba phần: lính chết theo quốc gia, dân thường chết (gồm Holocaust), rồi đặt Thế chiến II cạnh các cuộc chiến khác. Người xem có thể dừng lại để tự xem biểu đồ, và phim được khen là làm số người chết trở nên **"all too comprehensible"** (dễ hiểu đến đau lòng) ([History News Network](https://historynewsnetwork.org/article/160255)). Các nguồn ghi độ dài khác nhau (15 hoặc 19 phút), có lẽ vì có nhiều phiên bản. Đây là bằng chứng gần nhất với kênh của bạn. Một người, làm bằng code, kể một bi kịch có thật bằng hình đếm được, và đạt hàng triệu lượt xem.

Lộ tỉ lệ cũng có một luật rõ. Kurzgesagt zoom vào cái rất nhỏ và ra cái rất lớn, nhưng khác "Powers of Ten" ở chỗ **luôn so với cỡ người ở mỗi bước**. Khi hình người khuất khỏi khung, người xem mất cảm giác độ lớn, chỉ còn lại ý "this is really big and that is really small" ([FlowingData](https://flowingdata.com/2023/12/21/scale-of-all-the-things-compared-to-you/)). Áp vào Titanic **(KN)**: khi lộ cỡ con tàu, giữ một hình người nhỏ trên boong. Khi lộ tảng băng, giữ con tàu làm mốc. Khi lộ độ sâu nơi xác tàu nằm, giữ một mốc quen thuộc (một tòa nhà) đứng cạnh cột nước.

Chuyển cảnh là chất nối của truyện, không phải trang trí. Blazer nhắc **"never underestimate the power of the animated transition!"**, vì hoạt hình đi từ cảnh này sang cảnh khác được mà không cần cắt ([Motionographer](https://motionographer.com/2016/01/18/tidying-up-for-the-muse-interview-with-liz-blazer-author-of-animated-storytelling/)). Graphic match nối hai cảnh khác nhau bằng cùng một bố cục hoặc màu ([Vaia](https://www.vaia.com/en-us/explanations/media-studies/filmmaking/graphic-match/)). Trong spot RBC của Motion Theory, chuyển cảnh **củng cố chính thông điệp** về sự kết nối ([Motionographer](https://dev.motionographer.com/?p=12349)). Chuỗi "một shot giả" (prologue Rocknrolla, spot Nike) đi liền một mạch bằng chuyển động máy và cần một storyboard chắc ([Mattrunks](https://mattrunks.com/en/blog/motion/the-art-of-transition-in-video)). Ben Marriott morph giữa hai hình bằng shape cơ bản cộng điểm di chuyển, và phác blob thô trước khi làm chuyển cảnh lỏng ([Lester Banks](https://lesterbanks.com/2019/08/how-to-morph-between-any-two-shapes-in-after-effects/)). Trong code, thư viện **flubber** (giấy phép MIT) nội suy giữa hai path SVG bằng `interpolate(from, to, {maxSegmentLength: 10})`. Thư viện có thêm `separate` để tách một hình thành nhiều hình (tác giả nói hàm này "isn't terribly performant") và `combine` để gộp ngược lại ([flubber GitHub](https://github.com/veltman/flubber)). Đây đúng là công cụ cho ẩn dụ bi kịch kiểu **(KN)**: một con tàu tách thành 20 thuyền cứu sinh, rồi các thuyền tách thành hình người.

Nhìn chung **(KN)**, chuyển cảnh có ba loại nghĩa. Morph nói "cái này *trở thành* cái kia" (tàu thành xác tàu, đám đông thành con số). Match nói "cái này *giống* cái kia" (ánh đèn boong khớp với pháo sáng cứu nạn). One-shot liền mạch nói "đây là *một* dòng thời gian không gián đoạn", hợp cho chuỗi đêm chìm tàu. Còn cắt thẳng nói "có gì đó vừa vỡ". Luật sáu của Walter Murch xếp **cảm xúc (51%) và truyện (23%) trên nhịp, đường mắt và không gian** khi chọn cú cắt ([FilmDaft](https://filmdaft.com/walter-murchs-rule-of-six-the-editors-formula-for-choosing-the-right-cut/)). Bruce Block cho phép điều khiển cường độ bằng **tương phản và tương đồng** trên bảy thành phần: không gian, đường nét, hình khối, sắc độ, màu, chuyển động và nhịp ([O'Reilly](https://www.oreilly.com/library/view/the-visual-story/9781317745693/xhtml/Ch02.xhtml)). Motion bằng code điều khiển được cả bảy thành phần này bằng tham số.

Trừu tượng hóa cái chết là con dao hai lưỡi. Giới nghiên cứu cho rằng hoạt hình trong phim tài liệu có thể là phương tiện phù hợp để thể hiện chấn thương, như "Waltz with Bashir". Phim này kết bằng cách đặt hoạt hình cạnh cảnh quay thật về vụ thảm sát, và một bài viết gọi những giây đó là "a death scene" ([AUT repository](https://openrepository.aut.ac.nz/items/3f0ad085-825e-4419-9924-f32e3bd1bb3f)). Trừu tượng tạo một khoảng cách giúp người xem tiếp nhận chủ đề nặng, nhưng cũng có thể làm nhạt sức nặng. Ý này chưa xác minh được đúng tài liệu nào nói. Cách giữ sức nặng **(KN)** là tách hai tầng. Tầng con số dùng hình đếm được và trung tính. Tầng con người thì chọn một người có thật, có tư liệu, kể ở cỡ người (báo cáo trước dùng ví dụ thợ làm bánh Charles Joughin, kể lời khai *như là lời khai*). Không vẽ khoảnh khắc chết. Hình người đổi màu hoặc rơi khỏi hàng là đủ. Cách này cũng đúng luật quảng cáo: YouTube vẫn cho quảng cáo đầy đủ với nội dung giáo dục về thảm kịch nếu ít hoặc không chiếu bạo lực và không mang tính khai thác ([YouTube Help](https://support.google.com/youtube/answer/6162278)). Một lợi thế nữa của motion thuần: nội dung không trông như thật, "such as animation", thì không bắt buộc gắn nhãn nội dung tổng hợp ([YouTube Help](https://support.google.com/youtube/answer/14328491)).

Màu là đường cảm xúc chạy dọc cả tập. Color script của Pixar (bắt đầu từ Ralph Eggleston ở *Toy Story*) cho màu đậm lên khi cảm xúc mạnh và dịu đi ở khoảnh khắc u buồn ([MoMA](https://www.moma.org/audio/playlist/192/2581)). Phim nói chung tối dần qua các thập niên, nhưng hoạt hình vẫn giữ sáng ([Cutting et al., PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3485803/)). Vì vậy kênh motion không cần tối thui mới thành bi kịch. Trong code, color script trở thành **một hàm màu theo thời gian của cả tập**, nên mọi cảnh tự lấy màu đúng vị trí trên đường cảm xúc **(KN)**.

## Lời dẫn đặt nhịp, easing đặt cảm xúc, khoảng lặng đặt sức nặng

Con số chắc chắn duy nhất về thời lượng chuyển động đến từ thiết kế giao diện, không từ phim. Material Design (bản 1) đặt chuyển động trên điện thoại khoảng **300 ms**, chuyển cảnh lớn toàn màn hình tới **375 ms**, phần tử vào **225 ms**, phần tử ra **195 ms**, và cảnh báo "transitions that exceed 400ms may feel too slow". Vật đi xa hơn thì thời lượng dài hơn ([Material Design](https://m1.material.io/motion/duration-easing.html)). Material có bốn đường cong. **Standard** `cubic-bezier(0.4,0,0.2,1)` tăng tốc nhanh, giảm tốc chậm. **Deceleration** `(0,0,0.2,1)` vào khung ở tốc độ tối đa rồi chậm dần tới dừng. **Acceleration** `(0.4,0,1,1)` rời khung ở tốc độ tối đa. **Sharp** `(0.4,0,0.6,1)` dùng cho phần tử có thể quay lại (cùng nguồn). Material 3 có các mốc thời lượng từ 50 ms tới 550 ms, mỗi bậc cách 50 ms ([material-components-android](https://github.com/material-components/material-components-android/blob/master/docs/theming/Motion.md)). Joey Korenman giải thích vì sao ease trông tự nhiên: vật khởi động chậm, tăng tốc rồi giảm tốc giống vật lý đời thật; hiểu luật rồi thì phá luật để ra cảm giác cách điệu ([School of Motion](https://www.schoolofmotion.com/tutorials/intro-to-the-graph-editor-in-after-effects/)). Các nguyên tắc có tên là ease in/out, anticipation, overshoot, follow-through, hold và settle ([Figma](https://www.figma.com/blog/principles-in-motion/), chỉ có đoạn trích).

Không tìm thấy nguồn nào lập bảng "đường cong nào ra cảm xúc nào". Một nghiên cứu về đồ thị cảm xúc cho chu kỳ đi bộ kết luận rằng nhịp cảm xúc vẫn phụ thuộc tay nghề animator ([IIUM](https://irep.iium.edu.my/55224/)). Vì vậy bảng dưới hoàn toàn là **(KN)**. Logic của nó như sau. Nếu giao diện coi trên 400 ms là chậm, thì trong phim kể chuyện, chuyển động kéo dài nhiều giây cộng với giữ yên sẽ đọc thành trang nghiêm. Ngược lại, chuyển động rất ngắn rời khung ở tốc độ tối đa sẽ đọc thành đột ngột. Hãy coi con số Material là **cận dưới**: video xem trên màn lớn, có lời dẫn, cần chậm hơn giao diện.

| Cảm xúc (KN) | Thời lượng chuyển động | Đường cong | Nảy (overshoot) | Giữ yên sau đó |
|---|---|---|---|---|
| Kể thường, tò mò | 0,4–0,8 s | ease-out mềm (deceleration) | nhẹ được (chủ đề nhẹ) | 1–2 s |
| Căng, đe dọa | 1,5–3 s, tiến rất chậm | ease-in kéo dài, gần tuyến tính | không | không, tiếp tục dâng |
| Sốc, va chạm | 0,1–0,25 s hoặc cắt thẳng | acceleration, không giảm tốc | không; rung 2–4 khung | 0,5–1 s im |
| Bi thương, mất mát | 1,5–4 s | ease in-out rất mềm | **cấm** | 2–4 s |
| Suy ngẫm, kết | 3–8 s, máy đẩy chậm | gần tuyến tính, ease đầu cuối | cấm | đến hết câu dẫn |

Nhịp lấy từ lời dẫn. Ở Kurzgesagt, giọng đọc đặt timing cho đội animation, và quy trình là nghiên cứu, kịch bản, phác ẩn dụ, minh họa, giọng và animation, rồi mới đến nhạc và SFX ([Kurzgesagt](https://kurzgesagt.org/youtube/)). Animatic là storyboard có timing, kèm tiếng tạm và máy quay đơn giản, làm ra để thử nhịp trước khi animate ([Dreamina/CapCut](https://dreamina.capcut.com/ai-video/animatics), nguồn thương mại). Thứ tự giữa styleframe và storyboard thì các nguồn không thống nhất ([Boords](https://boords.com/blog/what-are-style-frames-definition-and-examples); [UPSI](https://ejournal.upsi.edu.my/index.php/JCIT/article/download/12395/6248/63976)). Với một người làm, hãy chốt **một styleframe kênh** một lần, rồi mỗi tập đi theo thứ tự: kịch bản, lời dẫn đã thu, animatic, animation **(KN)**. Code làm animatic gần như miễn phí. Dùng mốc từng từ của TTS để đặt các khối màu và chữ đúng chỗ, xem lại nhịp, rồi mới thay khối bằng đồ họa thật.

Ba luật nhịp từ báo cáo trước vẫn đúng với motion. Thứ nhất, tiếng va chạm nghe nặng nhờ **khoảng lặng ngay trước nó**, không nhờ âm lượng ([IRPR](https://sounddesign.irpr.agency/guides/how-to-add-weight-to-impacts/)). Trong motion, khoảng lặng của hình cũng vậy: hình đứng yên 0,5–2 s trước cú lộ con số **(KN)**. Thứ hai, nhạc tài liệu về bi kịch "has to be very scaled back" (phải tiết chế rất nhiều) ([motionpictures.org](https://www.motionpictures.org/2015/11/composer-kerry-muzzey-scoring-intimate-doc-seer/)). Nhạc rút đi ngay lúc con số nặng nhất được nói ra, và hình cũng nên ngừng chuyển động lúc đó **(KN)**. Thứ ba, khi mix, nhạc nằm thấp hơn giọng **12–20 dB** ([Sonilo](https://sonilo.com/blog/how-to-add-background-music-to-a-video); [IRPR](https://sounddesign.irpr.agency/guides/how-to-mix-audio-for-youtube/)), Lemo-Opuscar để chênh khoảng 10 dB ([TECHNIQUE.md](https://raw.githubusercontent.com/lemomo-ai/lemo-opuscar/main/TECHNIQUE.md)), và bản cuối xuất khoảng **−14 LUFS, true peak −1 dBTP** ([MeterPlugs](https://meterplugs.com/blog/2019/09/18/youtube-changes-loudness-reference-to-14-lufs.html); [Youlean](https://youlean.co/?p=30813)). Vì code đã biết sẵn mốc lời, bạn có thể vẽ trước đường hạ nhạc thay cho compressor **(KN)**. Không tìm được nguồn uy tín về việc cắt theo mỗi phách hay mỗi hai phách nhạc. Gợi ý **(KN)**: đặt cú lộ lớn rơi vào phách mạnh hoặc chỗ ngừng của lời, còn chuyển động phụ thì không ép theo phách, để khỏi thành video ca nhạc.

Cung cảm xúc của một tập có thể mượn cấu trúc The Fallen **(KN)**. Mở ở cỡ người (một con người, một con tàu, một buổi sáng). Dựng con số tăng dần bằng hình đếm được. Tạo một cú lộ tỉ lệ hoặc một phép so sánh làm sốc. Rồi lùi ra xem hậu quả và bài học, với khoảng lặng. Phần khung kịch bản đã có nguồn ở báo cáo trước vẫn giữ nguyên. YouTube đo riêng phần trăm người còn xem sau **30 giây đầu**, và gắn chỉ số này với việc phần mở đầu khớp tiêu đề cùng ảnh thu nhỏ ([YouTube Help](https://support.google.com/youtube/answer/9314415?hl=en)). Các nhịp truyện phải nối bằng **"nhưng" và "vì thế"**, không bằng "rồi thì" ([Austin Kleon](https://tumblr.austinkleon.com/tagged/matt%20stone)). Sổ tay MrBeast đặt điểm móc lại quanh **phút 3 và phút 6** ([Netinfluencer](https://www.netinfluencer.com/mrbeast-productions-leaked-internal-document-rosanna-pansino/)). Lời dẫn đọc khoảng **130–150 từ/phút** tiếng Anh ([IRPR](https://sounddesign.irpr.agency/tools/voiceover-word-count-calculator/)). Motion có thêm một vai ở đây: mỗi chữ "nhưng" trong kịch bản nên có **một sự kiện hình** đi kèm (đổi màu, đổi tỉ lệ, đổi hướng chuyển động), để người xem *thấy* cú lật chứ không chỉ nghe **(KN)**.

**Bảng màu và chuyển động theo đoạn cho một tập thảm họa (KN)**

| Đoạn | Màu | Chuyển động chủ đạo | Chuyển cảnh | Người dẫn |
|---|---|---|---|---|
| Mở, hy vọng | vàng kem, ấm, tương phản thấp | trôi chậm, parallax 3–5 lớp | match, morph mềm | tò mò, cử chỉ mở |
| Dấu hiệu nguy hiểm | xanh đêm, tương phản tăng | ít, tiến chậm | cắt thẳng gọn | nhìn sang hình, khựng |
| Cao trào | đen + điểm sáng | ngắn, gấp; rung 2–4 khung | cắt gấp, cú đập ở khung đầu | ít lời, thở nhanh |
| Con số mất mát | xám xanh, bão hòa thấp | hình người đổi màu từng hàng | không chuyển cảnh, giữ một shot | đứng yên, mắt nhìn xuống |
| Kết | xám + một vật giữ màu ấm | máy đẩy rất chậm | dissolve chậm | nói nhỏ, một cử chỉ cuối |

## Người dẫn chuyện motion biết diễn: khối đơn giản, rig nhỏ, phản ứng thật

Lemo-Opuscar, bộ skill làm phim "without a video model" cho Claude Code, tự nhận rig 2.5D của nó chỉ **"enough for pantomime"** (đủ cho kịch câm), và tài liệu không mô tả cách khớp môi ([TECHNIQUE.md](https://raw.githubusercontent.com/lemomo-ai/lemo-opuscar/main/TECHNIQUE.md)). Đó chính là khoảng trống cần lấp. Câu trả lời không nằm ở việc làm nhân vật phức tạp hơn. Nó nằm ở năm bộ phận rig nhỏ, cộng với một nguyên lý diễn đúng.

### Thiết kế để dễ rig: khối đơn giản, mỗi bộ phận một lớp

Nhân vật dựng từ khối đơn giản thì animate dễ hơn ([AWN](https://www.awn.com/comment/1060769)). Phong cách Kurzgesagt dựa trên "rounded shapes and vibrant colors" ([Arts at Michigan](https://artsatmichigan.umich.edu/ink/2019/09/27/simple-bright-beautiful-the-work-of-kurzgesagt)). Báo cáo trước đã nêu phép thử bóng dáng: tô đen toàn bộ mà vẫn nhận ra nhân vật ([3dsense](https://3dsense.net/blogs/shape-language-in-character-design-communicating-through-geometry)). Quy ước nghề nói tròn là thân thiện, vuông là vững chãi, tam giác là nguy hiểm ([Binus DKV](https://binus.ac.id/bandung/dkv/2025/11/04/character-design-101-turning-simple-shapes-into-personality/)). Với người dẫn cho đề tài bi kịch, chọn khối tròn pha vuông **(KN)**. Mỗi bộ phận phải là một lớp riêng: đầu, thân, cánh tay trên, cánh tay dưới, bàn tay, mắt, mày, miệng. Trong code, mỗi lớp là một nhóm SVG hoặc một hàm vẽ canvas có điểm xoay (pivot) riêng.

Quay đầu 2.5D (hình phẳng trông như xoay trong không gian 3D) có một kỹ thuật chuẩn. Joysticks 'n Sliders đặt **5 tư thế: giữa, phải, trái, trên, dưới**, rồi tạo một "joystick" nội suy giữa chúng. Số pose là "no limit" và trộn được với nhau ([aescripts](https://aescripts.com/joystick-n-sliders)). Kỹ thuật này có một hạn chế. Góc chéo (ví dụ trên-trái) chỉ là trộn "trên" với "trái", nên có thể hỏng với hình chi tiết hoặc nét viền. Đây là phản ánh của người dùng năm 2018, có thể đã cũ ([Adobe Community](https://community.adobe.com/t5/after-effects-discussions/which-one-do-you-prefer-for-animating-bq-headrig-or-joystick-n-sliders/m-p/10181239)). Trong code **(KN)**, mỗi pose là một vector tham số (vị trí mắt, mũi, miệng, tai, độ rộng mặt). Joystick (x, y) trong khoảng [−1, 1] trộn giữa/trái/phải theo x và giữa/trên/dưới theo y. Nếu góc chéo hỏng thì thêm pose riêng cho góc chéo.

Bộ hình miệng có chuẩn rõ. Rhubarb Lip Sync dùng **6 hình cơ bản A–F**. A là môi khép cho P, B, M. B là miệng hé, răng cắn, dùng cho đa số phụ âm. C là miệng mở cho nguyên âm EH, AE. D là há rộng cho AA. E là hơi tròn cho AO, ER. F là chúm môi cho UW, OW, W. Có thêm **3 hình tùy chọn**: G (răng trên chạm môi dưới, cho F, V), H (âm L kéo dài) và X (nghỉ) ([Rhubarb GitHub](https://github.com/DanielSWolf/rhubarb-lip-sync)). Adobe Character Animator dùng **14 hình miệng**: 3 hình lúc im (Neutral, Smile, Surprised) và 11 viseme theo âm ([Adobe Community](https://community.adobe.com/t5/character-animator/what-is-the-standard-list-of-ch-mouth-positions/td-p/9275855); [Adobe](https://www.adobe.com/learn/adobe-character-animator/web/lip-sync-mouth-shapes)). Không có studio nào công bố "bao nhiêu biểu cảm là đủ". Bộ tối thiểu gợi ý **(KN)**: đầu 3 góc (thẳng, ba phần tư trái, ba phần tư phải) cộng 5 pose nội suy; miệng 9 hình kiểu Rhubarb, nhân hai cho "miệng buồn" và "miệng thường"; mày 5 tư thế (bình thường, nhướng, cau, buồn với đầu trong lông mày nâng lên, giận); mắt 4 trạng thái (mở, nhắm, nửa khép, nhìn lệch); bàn tay 5 hình thay được (mở, nắm, chỉ, ngửa tay trình bày, đặt lên ngực).

### Rig: năm khái niệm, viết lại bằng code

Các công cụ rig của After Effects và web đều quy về vài khái niệm, và mỗi khái niệm đều viết lại được bằng code. **IK hai xương** (tay, chân): Spine có IK constraint xoay xương để đầu xương chạm vào xương đích, kiểu 1 xương hoặc 2 xương. Lưu ý IK không có ở bản Spine Essential ([Spine](https://en.esotericsoftware.com/spine-ik-constraints)). IK hai xương 2D có lời giải đóng, hiệu quả hơn cách giải lặp. Lời giải này cần chọn hướng gập, và nếu đích ngoài tầm với thì trả về điểm gần nhất ([Ryan Juckett](https://ryanjuckett.com/analytic-two-bone-ik-in-2d)). Godot giải bằng định lý cosin trên tam giác gốc, khớp, đích, có tùy chọn lật hướng gập ([Godot docs](https://docs.godotengine.org/en/4.5/classes/class_skeletonmodification2dtwoboneik.html)). **Ống cong kiểu RubberHose**: "Hose Length" là khoảng cách pixel giữa hai đầu mà ở đó ống thẳng hoàn toàn; hai đầu gần hơn thì ống cong. "Realism" 100% làm ống bật thẳng như IK. "Roundness" 0% là gập nhọn, 100% là cong mượt ([Battleaxe](https://help.battleaxe.co/rubberhose3/controls), trang ghi không còn bảo trì). **Trộn pose**: Rive có state "1D blend" trộn nhiều timeline bằng một đầu vào số, và tài liệu Rive nêu "dynamic face rigs" là một ứng dụng ([Rive docs](https://rive.app/docs/editor/state-machine/states), qua đoạn trích). **Lớp biểu cảm cộng dồn**: báo cáo trước ghi một bẫy trong rig Rive: đầu vào "smile" ở 100% đè hết khẩu hình, nên biểu cảm phải cộng dồn ([Rive forum](https://rive.app/community/forums/support/fsnLLkXUaA62/blending-between-inputs/ftNEp8TkjtJb)). **Vật lý phụ** (tóc, áo, tai): Spine 4.2 có physics constraint, nhưng người dùng báo lỗi physics trông cứng ở runtime web ([Esoteric forum](https://it.esotericsoftware.com/forum/d/26653-spine-ts-physics-not-being-applied-web)).

Ánh xạ sang code như sau, toàn bộ là **(KN)**. IK: kẹp khoảng cách d vào [|L1−L2|, L1+L2−ε]. Góc khuỷu là `acos((L1²+L2²−d²)/(2·L1·L2))`. Góc vai là `atan2(dy,dx) ∓ acos((L1²+d²−L2²)/(2·L1·d))`, trong đó dấu ∓ là hướng gập. Ống cong: vẽ Bezier giữa vai và cổ tay. Khi d nhỏ hơn Hose Length, đẩy điểm điều khiển ra vuông góc sao cho độ dài cung xấp xỉ Hose Length. Trộn pose: nội suy tuyến tính hoặc song tuyến giữa các vector tham số. Mặt: nếu hai hình có cùng số điểm thì morph, khác số điểm thì đổi hình (swap). Vật lý phụ: lò xo `x'' = −k(x−target) − c·x'` với tần số riêng khoảng 2–4 Hz và tỉ số giảm chấn 0,3–0,6. Hai luật kỹ thuật quan trọng cho render từng khung **(KN)**. Một là lò xo phải tính tất định: hoặc tích phân lại từ khung 0 với bước cố định (ví dụ 1/120 s), hoặc dùng `spring()` của Remotion vốn là hàm của số khung. Hai là mọi ngẫu nhiên (chớp mắt, line boil) phải dùng hạt giống cố định, để render lại ra đúng hình cũ.

Nếu không muốn tự viết rig, có hai lựa chọn chạy được trên web. **Spine** có spine-ts với backend WebGL, Canvas và three.js. Bản WebGL đủ tính năng; bản Canvas không có mesh, clipping và tint màu ([spine-ts](https://en.esotericsoftware.com/git/runtimes/spine-ts)). **Rive** có gói chính thức `@remotion/rive` để nhúng vào Remotion ([Remotion API](https://www.remotion.dev/api)). Chưa xác minh được cách điều khiển đầu vào state machine của Rive theo số khung trong Remotion, nên hãy thử một cảnh 10 giây trước khi chốt. Lời khuyên **(KN)** cho một người làm cùng Claude Code: tự viết rig bằng SVG hoặc canvas. Bạn chỉ cần IK hai xương, lò xo, trộn pose và đổi hình. Tất cả đều là code thuần mà agent đọc, sửa và kiểm được. Rive hay Spine đáng dùng khi bạn muốn vẽ và chỉnh rig trên một editor có giao diện.

Học khái niệm rig ở đâu: Duduf (tác giả Duik) có hướng dẫn video miễn phí khoảng **5 giờ** cho Duik Ángela, gồm chương "The Auto-rigger, the Controllers, the limbs and the IK" và "Procedural animation". Khóa chính thức khoảng 11 giờ, giá gợi ý €75 ([RxLaboratorio](https://rxlaboratorio.org/rx-tutorial/duik-17-user-guide/); [RxLaboratorio](https://rxlaboratorio.org/rx-tutorial/duik-17/)). Ngoài ra có Rigging Academy của School of Motion ([School of Motion](https://schoolofmotion.com/rigging-academy)), Deekay Tool Rigging & Motion (28 bài, hơn 5 giờ) ([Motion Design School](https://motiondesign.school/courses/deekay-tool-rigging-animation/)), và chuỗi "Animating With Character" của Jake Bartlett ([Skillshare](https://www.skillshare.com/en/classes/animating-with-character-rigging/1435213963)). **Cảnh báo an toàn**: link cũ `rainboxlab.org/tools/duik/` hiện **chuyển hướng (301) sang tên miền lạ `w88resmi8.com`**, có vẻ tên miền đã bị chiếm. Đừng mở link đó; chỉ dùng rxlaboratorio.org. Cũng tránh các trang "tải khóa học miễn phí", vì đó có thể là bản lậu.

### Diễn: không bao giờ đứng yên, và phản ứng quan trọng hơn cử động

Nguyên lý diễn của báo cáo trước vẫn là xương sống. Ed Hooks viết **"Thinking tends to lead to conclusions, and emotion tends to lead to action"** và **"Acting is doing; acting is also reacting"** ([Acting Coach Scotland](https://www.actingcoachscotland.co.uk/blog/principles-acting-animators-and-actors)). Theo ông, cảm xúc đứng một mình có "zero theatrical currency"; khán giả chỉ đồng cảm khi thấy nhân vật *làm* một việc ([Ed Hooks](https://www.midnighteast.com/mag/?p=4216)). Với người dẫn, nghĩa là lúc kể dữ kiện thì ít cử chỉ, còn lúc có cảm xúc thì có *một* hành động rõ: ngừng lại, cúi đầu, hạ tay. Người dẫn quay sang nhìn hình lịch sử rồi khựng lại sẽ sống hơn nhiều so với nói thẳng vào máy suốt.

Lớp "sống" đến từ moving hold. Moving hold "animates between two very similar positions": kể cả nhân vật ngồi yên vẫn thở hoặc đổi tư thế rất nhẹ, để khỏi trông "lifeless" ([Wikipedia](https://en.wikipedia.org/wiki/Twelve_basic_principles_of_animation)). Idle tốt bắt đầu bằng **vòng thở**, chồng thêm lắc đầu nhẹ và phụ kiện đung đưa, đổi nhịp và tần suất, không lặp cùng một cử động ([AnimSchool](https://blog.animschool.edu/2024/06/14/breathing-life-into-idle-animations)). Moving hold có bốn loại: quán tính, thở, liếc mắt, đỡ đầu. Lỗi hay gặp là quên quán tính của động tác trước; độ trôi nhẹ nên đi theo hướng của quán tính gần nhất ([AnimSchool](https://blog.animschool.edu/tag/idle-loop)). Ben Marriott dùng overlapping action để vật thể "feel alive" ([Adobe MAX 2022](https://www.adobe.com/max/2022/sessions/apac-behind-the-magic-engaging-animation-and-motio-s907.html)). Trong code, cách đúng là **cộng nhiều sóng với chu kỳ không chia hết cho nhau** (ví dụ 3,7 s; 5,3 s; 8,1 s), để vòng idle không bao giờ lặp lại y hệt **(KN)**.

Mắt có số đo thật (từ báo cáo trước). Người chớp khoảng **17 lần/phút khi nghỉ, 26 lần khi trò chuyện** ([Bentivoglio et al.](https://wicri-demo.istex.fr/Wicri/Sante/explor/MovDisordV3/Site/fr/Main/Exploration/bibRecord.php?hk=005409)). Một cái chớp thường trong hoạt hình là **đóng 2 khung, giữ 1, mở 3**; chớp dài là đóng 3, giữ 2, mở 4. Nên chớp khi quay đầu, khi nhận ra điều gì, hoặc sau một cái nhìn lâu ([Bloop Animation](https://www.bloopanimation.com/blinking-animation/)). Chớp thật không đối xứng ([Disney Research](https://la.disneyresearch.com/wp-content/uploads/Modeling-and-Animating-Eye-Blinks-Paper.pdf)). Người buồn thật thường thu mình ([Animation Mentor](https://animationmentor.com/blog/the-6-basic-emotions-animating-sadness-with-tim-ingersoll)). Mặt buồn mà cổ cứng thì trông như máy ([Binus DKV](https://binus.ac.id/bandung/dkv/2025/11/03/building-emotion-through-movement-how-animators-make-you-feel/)).

Con số diễn sau đây chưa có nguồn đo, là **(KN)** để bắt đầu thử. Thở: thân co giãn dọc 1–2% (vai lên 2–4 px ở nhân vật cao khoảng 600 px). Chu kỳ thở 3–4 s khi bình thường, 1,5–2 s khi sợ, 5–6 s và vai thấp khi buồn. Overlap: vai, khuỷu, bàn tay trễ nhau 1–3 khung; đầu dừng trước, tóc vượt rồi lắng. Cử chỉ khi dẫn chuyện: đặt vào âm nhấn của câu; tay bắt đầu chuẩn bị trước âm nhấn khoảng 4–6 khung; giữa hai cử chỉ thì giữ tư thế bằng moving hold, không quay về tư thế gốc sau mỗi câu. Buồn trong phong cách phẳng: bóng dáng là chính (đầu cúi, vai rũ, thân thu nhỏ, chuyển động chậm và ít); đầu trong lông mày nâng lên là tín hiệu buồn mạnh nhất với mặt đơn giản. Sợ: vai nhô, tay thu vào thân, đồng tử nhỏ, run nhanh với biên độ nhỏ. Để giữ nhịp làm việc của một người, dùng hoạt hình giản lược. Vẽ "cách 2 khung" (12 hình/giây ở 24 fps) là chuẩn hoạt hình truyền hình Mỹ ([iD Tech](https://www.idtech.com/blog/what-does-animating-on-ones-twos-and-threes-mean)). Trong code, chỉ cần làm tròn số khung xuống số chẵn trước khi tính tư thế nhân vật. Riêng máy quay và đồ họa thì vẫn chạy mượt từng khung **(KN)**.

### Khớp môi: Rhubarb cho hình miệng, TTS cho mốc thời gian

Rhubarb xuất ra TSV (mỗi dòng gồm thời điểm và hình miệng), XML hoặc JSON (mảng `mouthCues` có `start`, `end`, `value`). Có thể tắt 3 hình mở rộng bằng tùy chọn `extendedShapes`. Bộ nhận dạng mặc định PocketSphinx chỉ hiểu tiếng Anh. Bộ **Phonetic** nhận theo âm, kém chính xác hơn nhưng dùng được cho mọi ngôn ngữ, kể cả tiếng Việt ([Rhubarb GitHub](https://github.com/DanielSWolf/rhubarb-lip-sync)). Chưa có nguồn đo độ chính xác của Phonetic với tiếng Việt. Về TTS, ElevenLabs có endpoint `/v1/text-to-speech/{voice_id}/with-timestamps`. Endpoint này trả audio kèm `alignment`, gồm ba mảng song song: ký tự, thời điểm bắt đầu và thời điểm kết thúc tính bằng giây ([ElevenLabs](https://elevenlabs.io/docs/api-reference/text-to-speech/convert-with-timestamps)). Azure trả sự kiện viseme có `audioOffset` tính bằng tick 100 ns ([Microsoft Learn](https://learn.microsoft.com/sr-cyrl-rs/azure/ai-services/speech-service/how-to-speech-synthesis-viseme)), nhưng người dùng báo có viseme sớm, có viseme trễ so với audio ([Microsoft Q&A](https://learn.microsoft.com/en-us/answers/questions/545767/azure-speech-sdk-viseme-audio-offset)). Luật thời điểm có nguồn nghề: hàm mở **trước âm thanh 1–2 khung**, và các âm B, M, P phải đóng miệng chính xác ([Pluralsight](https://www.pluralsight.com/resources/blog/software-development/proven-tips-animating-believable-lip-sync)).

Quy trình đơn giản nhất **(KN)**: chạy Rhubarb trên file audio cuối (kể cả giọng TTS đã xuất). Ở mỗi khung, tìm cue có `start ≤ t < end` sau khi đã dời sớm 1–2 khung, rồi đổi hình miệng. Giữ mỗi hình tối thiểu 2 khung để khỏi nhấp nháy. Thêm một khung chuyển tiếp giữa hai hình quá khác nhau (D sang A). Cuối cùng, cộng hình miệng với lớp cảm xúc, ví dụ khóe miệng trễ xuống khi buồn, chứ không thay thế. Với nhân vật phẳng, không cần khớp môi tuyệt đối. Mở và đóng đúng nhịp âm tiết, khép đúng ở P, B, M là đủ thuyết phục. Thêm một mẹo diễn **(KN)**: những đoạn bi thương nhất có thể để người dẫn *không nói trên hình*. Người dẫn đứng nhìn hình, lời dẫn vang như giọng kể ngoài khung. Cách này vừa né giới hạn khớp môi, vừa đúng tinh thần "phản ứng" của Hooks.

**Bảng trạng thái diễn cho người dẫn (KN)**

| Trạng thái | Thân | Đầu và mắt | Mày, miệng | Thở | Cử chỉ |
|---|---|---|---|---|---|
| Kể dữ kiện | thẳng, moving hold | nhìn máy, chớp 2–4 s | bình thường | 3–4 s | 0–1 cử chỉ mỗi câu, rơi vào từ khóa |
| Trình bày hình | xoay ba phần tư về phía hình | nhìn theo vật | nhướng nhẹ | 3–4 s | ngửa tay về phía hình |
| Nhận ra điều xấu | khựng 6–10 khung | liếc sang, rồi chớp | mày cau, miệng khép | ngừng thở một nhịp | tay dừng giữa chừng |
| Bi thương | vai rũ, thu nhỏ 2–3% | cúi, mắt nhìn xuống, chớp chậm | đầu trong lông mày nâng | 5–6 s | không, hoặc tay đặt lên ngực |
| Kết, suy ngẫm | đứng yên | nhìn xa, rồi về máy | gần bình thường | 4–5 s | một cử chỉ cuối, chậm |

## Dựng bằng code: một nguồn nhịp, khung là hàm của thời gian

Khung code có ba lựa chọn chín. **Remotion** là React; mọi chuyển động phải lấy từ `useCurrentFrame()`, và cách animate nào khác đều cần một bản tích hợp để đồng bộ thời gian ([Remotion](https://www.remotion.dev/docs/third-party)). Remotion có gói chính thức cho Lottie, Rive và three.js ([Remotion API](https://www.remotion.dev/api)). Giấy phép miễn phí cho cá nhân và công ty vì lợi nhuận **tối đa 3 người** ([LICENSE.md](https://github.com/remotion-dev/remotion/blob/main/LICENSE.md)). Nhóm lớn hơn trả gói Creators **25 USD/seat/tháng** ([Remotion pricing](https://www.remotion.dev/docs/license/pricing)). **Motion Canvas** là TypeScript, viết timeline bằng generator và có editor xem trước. Nó nhắm đến animation giải thích đồng bộ với voice-over, miễn phí, mã nguồn mở ([Motion Canvas](https://motioncanvas.io/docs/)). Điểm đặc biệt là `waitUntil('event')`: mốc này hiện thành một "pill" trên editor để kéo cho khớp lời đọc, không cần ghi cứng số giây ([Motion Canvas time events](https://motioncanvas.io/docs/time-events)). Hạn chế là render bằng nút bấm trong giao diện. **Revideo**, bản fork của Motion Canvas, biến render thành một lời gọi hàm và cho deploy API render ([Revideo](https://docs.re.video/)), nhưng ít người dùng hơn nhiều ([pkgpulse](https://www.pkgpulse.com/guides/remotion-vs-motion-canvas-vs-revideo-programmatic-video-2026)). **Kiểu Lemo-Opuscar** là trang web có hàm `render(t)` tất định chạy trong Chrome không giao diện. Canvas 2D lo phần 2D, three.js lo 3D, shader WebGL2 lo hậu kỳ. Mặc định 1920×1080 ở 24 fps, `timeline.js` là nguồn nhịp duy nhất, và `cuecheck.py` kiểm độ lệch hình với nhạc, mục tiêu 0 ms ([TECHNIQUE.md](https://raw.githubusercontent.com/lemomo-ai/lemo-opuscar/main/TECHNIQUE.md)). Nên tránh Theatre.js làm lõi: Snyk xếp gói npm của nó vào loại "inactive", lần push gần nhất ghi nhận là 14/8/2024 ([Snyk](https://snyk.io/advisor/npm-package/theatre)).

| Tiêu chí | Remotion | Motion Canvas / Revideo | Trang `render(t)` kiểu Lemo-Opuscar |
|---|---|---|---|
| Agent viết và render tự động | mạnh nhất | Revideo được; Motion Canvas bấm nút | được, bạn tự giữ hạ tầng |
| Khớp lời đọc | từ dữ liệu timestamp | kéo "pill" bằng tay, rất tiện | từ `timeline.js` |
| Caption, bản đồ, số liệu | có `@remotion/captions` | tự viết | tự viết |
| Nhân vật | SVG/canvas tự viết, hoặc Rive/Lottie | SVG/canvas tự viết | canvas tự viết |
| Giấy phép | miễn phí đến 3 người | miễn phí | theo repo |

Lựa chọn gợi ý **(KN)**: nếu bạn làm một mình và muốn Claude Code tự lo từ đầu đến cuối, chọn **Remotion**. Code của nó tất định (cùng số khung cho ra cùng hình), nên kiểm được bằng cách render một khung tĩnh rồi xem ảnh. Nó cũng có sẵn caption và lò xo. Nếu bạn muốn tự tay chỉnh nhịp theo cảm giác, chọn **Motion Canvas**. Nếu đã quen Lemo-Opuscar, cứ giữ nó, rồi bổ sung phần rig mặt và khớp môi mô tả ở trên.

Timing lấy từ TTS theo một đường ống cố định. Lấy timestamp từng ký tự của ElevenLabs, gộp thành từ ở khoảng trắng, rồi đổi thành dạng `{text, startMs, endMs}` **(KN)**. Azure WordBoundary phát sự kiện ở đầu mỗi từ; đổi tick sang ms bằng `(AudioOffset + 5000) / 10000` ([Microsoft](https://learn.microsoft.com/it-it/dotnet/api/microsoft.cognitiveservices.speech.speechsynthesiswordboundaryeventargs?view=azure-dotnet)). Có lỗi đã biết: AudioOffset bằng 0 với một số giọng neural ([Microsoft Q&A](https://learn.microsoft.com/en-sg/answers/questions/1651510/azure-text-to-speech-wordboundary-event-always-ret)). `createTikTokStyleCaptions()` của Remotion gom token thành các trang chữ. `combineTokensWithinMilliseconds` quyết định bao nhiêu từ trên một trang; `breakOnSilenceAfterMilliseconds` ngắt trang ở chỗ lặng ([Remotion captions](https://www.remotion.dev/docs/captions/create-tiktok-style-captions)). Từ đó **(KN)**: mỗi nhịp trong kịch bản gắn một **từ kích hoạt**. Code tìm `startMs` của từ đó, đổi sang khung bằng `frame = round(ms / 1000 × fps)`, và đặt cue animation ở đó. Ở 24 fps, một khung là 41,7 ms; ở 30 fps là 33,3 ms. Khi đổi lời dẫn, chỉ cần chạy lại TTS; mọi cue tự dời theo, không phải sửa code cảnh.

Các con số chuyển động nên ghi thành luật trong một file hằng số dùng chung. Hàm `spring()` của Remotion mặc định `mass: 1, damping: 10, stiffness: 100`, có nảy; muốn bỏ nảy thì tăng damping; `durationInFrames` kéo giãn lò xo cho vừa số khung ([Remotion spring](https://www.remotion.dev/docs/spring)). Mã nguồn easings.net dùng hằng số back `c1 = 1.70158`, `c3 = c1 + 1`, easeOutExpo `= 1 − 2^(−10x)`, easeOutBack `= 1 + c3(x−1)³ + c1(x−1)²` ([easings.net source](https://raw.githubusercontent.com/ai/easings.net/master/src/easings/easingsFunctions.ts)). Material 3 "emphasized decelerate" là `cubic-bezier(0.05, 0.7, 0.1, 1.0)`, đi với khoảng 400 ms khi phần tử vào màn hình. Con số này lấy từ nguồn phụ, chưa kiểm với trang chính thức ([Fluid tokens](https://docs.liri.io/sdk/fluid/develop/structFluid_1_1MotionEasingTokens.html)). Quy đổi ở 24 fps: 200 ms khoảng 5 khung, 400 ms khoảng 10, 1 s là 24.

Thư viện component nên dựng một lần, dùng mọi tập **(KN)**. Gồm: `Narrator` (nhận props trạng thái, hướng nhìn, cue cử chỉ, cue miệng); `IsotypeGrid` (đếm hình, đổi màu, rơi khỏi hàng theo nhóm); `ScaleReveal` (zoom có neo hình người); `MorphTransition` (bọc flubber); `RouteMap` (đường đi trên bản đồ); `Counter` (bộ đếm số, có giữ yên ở số cuối); `ChapterTitle`; `Caption`; `ColorScript` (hàm màu theo thời gian); và `CameraRig` (parallax nhiều lớp, máy đẩy chậm, rung). Riêng bản đồ, D3 và các bộ chuyển cảnh có sẵn thì phiên nghiên cứu này chưa thu được nguồn. Có một rủi ro cần nhớ khi dùng lại component. Từ 15/7/2025, YouTube đổi chính sách "repetitious content" thành "inauthentic content", nhắm vào các video theo khuôn ít khác biệt đăng hàng loạt ([Search Engine Journal](https://www.searchenginejournal.com/youtube-monetization-update-spam-not-reaction-channels/550755/)). Component nên dùng lại cho *ngữ pháp*, còn mỗi tập phải có ẩn dụ chính, cú lộ tỉ lệ và người kể chuyện riêng.

## Bộ key sẵn dùng cho brief và cho agent viết code

Các khối dưới viết bằng tiếng Anh để dán thẳng vào brief hoặc vào lệnh cho Claude Code. Mọi con số trong khối là **(KN)**, trừ chỗ ghi "sourced".

**Key kể chuyện bằng chuyển động**

```
MOTION STORY KEYS
- Story first, style second. Every motion must state one idea in one sentence; if it explains nothing, cut it.
- One visual metaphor per scene, sketched before animating (sourced: Kurzgesagt).
- Write the channel's motion grammar before episode 1: screen direction, what living vs lost looks like,
  how facts enter, how memories leave. Break a rule only on purpose, at a story turn.
- Every "but" in the script gets one visual event (color shift, scale change, direction change).
- Transitions carry meaning: MORPH = "becomes", MATCH = "is like", ONE-SHOT = "one unbroken timeline",
  HARD CUT = "something broke".
- Narration sets the timing. Lock voice-over before animation; animatic before final art.
- Contrast follows the emotional arc: calm = similar shapes/colors/slow motion; climax = maximum contrast.
- Stillness is a tool: freeze motion 0.5-2 s before a big reveal; hold 2-4 s after a tragic number.
- Avoid "activity without meaning": no constant zooms, wiggles, or sound hits.
```

**Key con số và bi kịch**

```
TRAGEDY & NUMBERS KEYS
- Isotype rule (sourced): bigger quantity = MORE identical icons, never a BIGGER icon. Fixed value per icon.
- Pick a scale so every compared group is a near-whole number of icons; state the scale on screen.
- Counting is the emotion: reveal icons row by row in time with narration, not all at once.
- Loss = icon turns grey and falls out of the row. Never animate a death itself. No bodies, no gore.
- Every scale reveal keeps a human-sized anchor in frame (sourced: Kurzgesagt rule).
- Two layers: neutral counted icons for the number, one documented real person at human scale for the feeling.
- At the heaviest number: motion stops, music pulls back, narrator does not move.
- Respectful pacing: no overshoot, no bounce, no playful easing anywhere near loss of life.
```

**Key diễn cho người dẫn chuyện (lệnh cho agent)**

```
NARRATOR RIG & ACTING KEYS
- Layers: head, torso, upperArm/foreArm/hand (L,R), brows, eyes(L,R), mouth. Each layer has its own pivot.
- Head turn: 5 poses (center, left, right, up, down) as parameter vectors; bilinear blend from joystick
  (x,y) in [-1,1]. Add explicit diagonal poses if the blend breaks.
- Arms: analytic two-bone IK (law of cosines), clamp reach, choose bend direction per pose;
  or rubber-hose Bezier with hoseLength, roundness.
- Expressions are ADDITIVE layers on top of mouth shapes; never let "sad" or "smile" overwrite visemes.
- Never fully still: moving hold = breathing + head drift + sparse glances, summed sine waves with
  non-repeating periods (e.g. 3.7 s, 5.3 s, 8.1 s).
- Breathing: torso scaleY 1-2%; period 3-4 s normal, 1.5-2 s fear, 5-6 s grief.
- Blink: close 2 frames, hold 1, open 3 at 24 fps (sourced: Bloop); every 2-4 s while talking;
  blink on head turns and realizations; slow and rare in grief. Seeded random only.
- Overlap: shoulder > elbow > hand lag 1-3 frames; hair/collar on springs (2-4 Hz, damping ratio 0.3-0.6),
  deterministic from frame 0.
- Gestures land on stressed words; anticipation starts 4-6 frames before the word; hold the pose
  between gestures, do not reset to neutral after each sentence.
- Think = little motion. Feel = one clear action (stop, lower head, drop hands) (sourced: Ed Hooks).
- React to the history image: turn 3/4 toward it, look, pause, then speak.
- Grief: head down, shoulders drop, inner brows up, eyes low, no tears, no big gestures.
- Fear: shoulders up, hands close to body, small pupils, tiny fast tremor.
- Character on twos (12 poses/s at 24 fps); camera and graphics on ones.
```

**Key khớp môi**

```
LIP SYNC KEYS
- Mouth set: Rhubarb A-F + G, H, X (sourced). Two variants: neutral and sad.
- Source: Rhubarb JSON mouthCues on the final audio; Vietnamese -> phonetic recognizer.
- Shift mouth cues 1-2 frames EARLIER than audio (sourced); M/B/P must be fully closed.
- Minimum 2 frames per mouth shape; insert one in-between frame for D <-> A jumps.
- Mouth shape + emotion layer (corner down for sad) are combined, not swapped.
- In the heaviest moments the narrator may listen silently while the voice continues off-screen.
```

**Key con số chuyển động (hằng số dùng chung)**

```
MOTION CONSTANTS
fps = 24; frame(ms) = round(ms / 1000 * fps)
UI floor (sourced, Material, NOT film): enter 225 ms, exit 195 ms, large 375 ms, >400 ms "slow" for UI
Curves (sourced): standard (0.4,0,0.2,1); decelerate (0,0,0.2,1); accelerate (0.4,0,1,1); sharp (0.4,0,0.6,1)
Remotion spring default (sourced): mass 1, damping 10, stiffness 100 (bounces); raise damping to remove bounce
easeOutBack c1 = 1.70158 (sourced) -> light topics only
Film-level durations (rule of thumb): calm 0.4-0.8 s; dread 1.5-3 s; shock 0.1-0.25 s or hard cut;
  grief 1.5-4 s; reflection 3-8 s
Holds (rule of thumb): before reveal 0.5-2 s silence; after tragic number 2-4 s; text on screen >= 2 s
Shot length (rule of thumb): normal 3-6 s; tension 1-3 s; tragedy 6-12 s
Stagger (rule of thumb): 2-4 frames between UI-like elements; 0.3-0.6 s per row of counted icons
Camera shake (rule of thumb): 2-4 frames at impact, decays; never during grief
Music under voice (sourced): 12-20 dB; master -14 LUFS, -1 dBTP
```

**Lệnh mẫu cho Claude Code (dán đầu mỗi tập)**

```
CODING AGENT BRIEF
Build this episode as deterministic frame-rendered motion graphics (no video models).
1. Read script.yaml: each beat has {id, text, triggerWord, visualMetaphor, emotion, transition}.
2. Read timing.json from TTS (word timestamps). Map every triggerWord to a frame. This is the only clock.
3. First render an ANIMATIC: flat blocks + text at every cue, plus voice and temp music. Stop for review.
4. After approval, replace blocks with components: Narrator, IsotypeGrid, ScaleReveal, MorphTransition,
   RouteMap, Counter, ChapterTitle, Caption, CameraRig. Colors come from ColorScript(t).
5. Use MOTION CONSTANTS and NARRATOR keys above. All randomness seeded; springs deterministic.
6. Lip sync from rhubarb.json, shifted 2 frames early, emotion layer additive.
7. Self-check: render stills at every cue frame; check no element moves without a story reason,
   no overshoot near loss of life, every scale reveal has a human anchor, captions match audio.
8. Export 1920x1080, 24 fps; audio voice-first, music ducked by a pre-drawn curve, -14 LUFS / -1 dBTP.
```

**Checklist kể chuyện mỗi tập**

```
[ ] Ẩn dụ chính của tập viết được trong 1 câu; mỗi cảnh có 1 ẩn dụ hình
[ ] Ngữ pháp chuyển động của kênh được dùng đúng; chỗ phá luật đặt ở cú lật truyện
[ ] 30 s đầu chứng minh lời hứa của tiêu đề; mỗi "nhưng" có một sự kiện hình
[ ] Con số lớn = hình đếm được, có ghi tỉ lệ; lộ tỉ lệ luôn có hình người làm mốc
[ ] Có một người thật, có tư liệu, kể ở cỡ người; lời khai ghi là lời khai
[ ] Không vẽ khoảnh khắc chết; không nảy/đàn hồi gần chỗ mất mát
[ ] Màu đi theo color script; giảm bão hòa có lý do
[ ] Khoảng lặng: hình đứng yên trước cú lộ, nhạc rút ở con số nặng nhất
[ ] Điểm móc lại quanh phút 3 và phút 6; kết ngay sau khi trả lời câu hỏi lớn
[ ] Tập này có ẩn dụ và cú lộ riêng, không chỉ lắp lại component (tránh "inauthentic content")
```

**Checklist người dẫn chuyện**

```
[ ] Bóng dáng nhận ra ở cỡ ảnh thu nhỏ; khối tròn/vuông, mỗi bộ phận một lớp có pivot
[ ] Đủ bộ: 5 pose đầu, 9 miệng x 2 biến thể, 5 mày, 4 mắt, 5 bàn tay
[ ] Idle không bao giờ đứng yên và không lặp đều; thở đổi theo cảm xúc
[ ] Mỗi đoạn có ít nhất một phản ứng với hình (nhìn sang, khựng, im)
[ ] Cử chỉ rơi vào từ nhấn, chuẩn bị trước 4-6 khung, không về tư thế gốc sau mỗi câu
[ ] Miệng sớm 1-2 khung, M/B/P khép, mỗi hình >= 2 khung; cảm xúc là lớp cộng
[ ] Cảnh bi thương: cúi đầu, mày trong nâng, chớp chậm, không khóc lóc
[ ] Render lại cùng khung ra đúng hình cũ (ngẫu nhiên có hạt giống, lò xo tất định)
```

**Checklist pipeline code**

```
[ ] script.yaml có từ kích hoạt cho mọi nhịp; timing.json từ TTS là nguồn nhịp duy nhất
[ ] Animatic duyệt xong mới làm hình thật
[ ] Hằng số chuyển động nằm trong một file; không có số thời lượng viết rời trong cảnh
[ ] Render khung tĩnh ở mọi cue để kiểm; kiểm độ lệch hình-tiếng = 0 khung
[ ] Không dùng Theatre.js làm lõi; giấy phép Remotion kiểm lại nếu nhóm >= 4 người
[ ] Tài liệu Duik chỉ lấy từ rxlaboratorio.org; KHÔNG mở rainboxlab.org (chuyển hướng lạ)
[ ] Xuất 1920x1080, 24 fps; -14 LUFS, -1 dBTP; nghe thử trên loa điện thoại và ở mono
```

## Bảng tách số có nguồn và số kinh nghiệm

| Con số | Giá trị | Trạng thái |
|---|---|---|
| Hình đếm được Halloran | 1 hình = 1.000 người; hơn 4 triệu lượt xem | có nguồn |
| Sai số tỉ lệ Isotype (Bilston) | thiếu ~21,9% / dư ~56,2% | có nguồn (đoạn trích) |
| Material: vào / ra / lớn | 225 / 195 / 375 ms; trên 400 ms là chậm | có nguồn, **cho giao diện** |
| Đường cong Material | 4 bộ cubic-bezier | có nguồn |
| Remotion spring | mass 1, damping 10, stiffness 100 | có nguồn |
| Hằng số back của easing | 1,70158 | có nguồn |
| Quay đầu | 5 pose nội suy | có nguồn (công cụ JnS) |
| Hình miệng | Rhubarb 6 + 3; Character Animator 3 + 11 | có nguồn |
| Miệng mở sớm | 1–2 khung | có nguồn (blog nghề) |
| Chớp mắt | 17/phút nghỉ, 26/phút nói; 2-1-3 khung | có nguồn |
| Vẽ cách 2 khung | 12 hình/giây ở 24 fps | có nguồn |
| Lemo-Opuscar | 24 fps, 1920×1080, −14 LUFS, rig "đủ cho kịch câm" | có nguồn (repo) |
| Giấy phép Remotion | miễn phí đến 3 người; 25 USD/seat/tháng | có nguồn |
| Nhạc dưới giọng; master | 12–20 dB; −14 LUFS, −1 dBTP | có nguồn (blog, hãng) |
| Thời lượng chuyển động theo cảm xúc | 0,4–0,8 / 1,5–3 / 0,1–0,25 / 1,5–4 / 3–8 s | KN |
| Giữ yên | 0,5–2 s trước cú lộ; 2–4 s sau con số bi kịch | KN |
| Thở | co giãn 1–2%; chu kỳ 3–4 / 1,5–2 / 5–6 s | KN |
| Lò xo phụ | 2–4 Hz, giảm chấn 0,3–0,6 | KN |
| Overlap; chuẩn bị cử chỉ | 1–3 khung; 4–6 khung | KN |
| Miệng giữ tối thiểu | 2 khung | KN |
| Rung khi va chạm | 2–4 khung | KN |
| Độ dài shot theo đoạn | 3–6 / 1–3 / 6–12 s | KN |

## Kết luận

Điều thay đổi khi bỏ video AI không phải là mất phần diễn, mà là phần diễn chuyển chỗ. Trong motion graphics, cảm xúc không đến từ khuôn mặt chân thật. Nó đến từ **quan hệ giữa chuyển động và thời gian**: hình đứng yên đúng lúc, con số hiện ra đúng nhịp lời, người dẫn khựng lại trước khi nói. Halloran đã chứng minh một người làm bằng code có thể khiến hàng triệu người cảm được một con số chết chóc, chỉ bằng hình đếm được, nhịp chậm và âm thanh. Người dẫn chuyện ở đây là lớp thứ hai cộng thêm vào công thức đó. Nó không cần diễn như diễn viên. Nó cần phản ứng như một người xem tử tế đứng cạnh khán giả.

Hệ quả thực tế là đầu tư nên dồn vào những thứ viết một lần, dùng mãi: ngữ pháp chuyển động của kênh, file hằng số timing, rig người dẫn với bảng trạng thái diễn, và đường ống TTS sang khung. Khi các thứ này đã ổn, mỗi tập chỉ còn hai việc thật sự sáng tạo: chọn ẩn dụ chính và chọn cú lộ tỉ lệ. Đó cũng chính là thứ giữ kênh khỏi bị xếp vào "nội dung theo khuôn". Điều chưa biết lớn nhất vẫn còn đó. Chưa có nguồn đo nào cho thời lượng chuyển động "đúng cảm xúc" trong phim kể chuyện, cũng chưa có nguồn đo độ chính xác khớp môi tiếng Việt bằng Rhubarb Phonetic. Hãy coi các bảng **(KN)** là giả thuyết, làm một cảnh thử 30 giây (một con số, một cú lộ tỉ lệ, một phản ứng của người dẫn), rồi chỉnh bằng mắt và bằng biểu đồ giữ chân của chính kênh.
