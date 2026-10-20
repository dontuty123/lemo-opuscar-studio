# Kể thảm họa bằng hoạt hình: luật giữ người xem

Chìa khóa của một video hoạt hình kể chuyện lịch sử nằm trước tiên ở **kịch bản và cách đóng gói**, sau đó mới tới hình ảnh. Ba mươi giây đầu phải giữ đúng lời hứa của tiêu đề và ảnh thu nhỏ, vì YouTube đo riêng tỷ lệ người còn xem sau 30 giây. Các nhịp truyện phải nối nhau bằng "nhưng" và "vì thế", không bằng "rồi thì". Lời dẫn đọc khoảng 130–150 từ mỗi phút, và hình được dựng theo bản lời đã thu, giống cách Kurzgesagt làm. Nhân vật dẫn chuyện trên hình là thứ hiếm: trong mẫu kênh lớn được khảo sát (Kurzgesagt, Simple History, The Infographics Show, OverSimplified, TED-Ed), không kênh nào dùng một MC hoạt hình hiện hình cố định. Thứ các kênh này giữ cố định là **giọng đọc**, như Steve Taylor đọc cho Kurzgesagt suốt hơn 12 năm. Nghĩa là bạn có một chỗ trống để chiếm, nhưng chưa có kênh nào chứng minh công thức này. Diễn xuất của người dẫn nên theo Ed Hooks: suy nghĩ thì ít cử động, cảm xúc mới sinh hành động, và phản ứng với hình lịch sử quan trọng hơn nói thẳng vào máy. Với đề tài bi kịch có thật, những nhà soạn nhạc giỏi đều tiết chế: nhạc dựa vào drone, nhịp đập và âm trầm thay cho giai điệu, và rút hẳn đi khi thông tin nặng nhất được nói ra. Khi mix, để nhạc thấp hơn giọng 12–20 dB, rồi xuất bản cuối khoảng −14 LUFS với true peak −1 dBTP. Về pipeline, cách hợp lý cho một người làm là kết hợp hai nhánh: Seedance (qua Magnific) cho cảnh người dẫn diễn và nói, còn code (Claude Code + canvas/WebGL, kiểu Lemo-Opuscar) cho bản đồ, số liệu, chữ, mở đầu và kết thúc. Lý do: video AI diễn mặt tốt hơn hẳn, còn code thì rẻ, đồng nhất và sửa được từng khung.

> **Cách đọc con số trong báo cáo.** Con số có link ngay sau là **có nguồn** (vẫn ghi rõ nếu nguồn chỉ là blog hay bên thứ ba). Con số đánh dấu **(KN)** là kinh nghiệm hoặc suy luận của người tổng hợp, chưa có nguồn đo; hãy coi đó là điểm xuất phát rồi chỉnh bằng biểu đồ giữ chân của chính kênh bạn. Bảng tổng hợp ở cuối báo cáo tách riêng hai loại này.

## Ba mươi giây đầu quyết định, và truyện phải chạy bằng "nhưng"

YouTube Studio có chỉ số **Intro**: phần trăm người xem còn ở lại sau **30 giây đầu**. YouTube gắn intro mạnh với việc phần mở đầu khớp tiêu đề và ảnh thu nhỏ, và khuyên creator "thử nghiệm 30 giây đầu". YouTube cũng khuyên so sánh với "typical retention" của **10 video gần nhất có độ dài tương tự** của chính kênh, chứ không so với một chuẩn chung nào ([YouTube Help](https://support.google.com/youtube/answer/9314415?hl=en)). Một bảng thuật ngữ bên thứ ba nói Studio xếp video có từ 50% người xem trở lên sau 30 giây vào nhóm "above typical intros". Thông tin này chưa được kiểm trên trang của YouTube, nên chỉ nên coi là nhãn giao diện ([Creator Essentials](https://www.creatoressentials.com/glossary/key-moments-for-audience-retention/)). Sổ tay sản xuất của MrBeast (bị lộ năm 2024) cho thấy phút đầu mong manh đến mức nào: "We lost 21 million viewers in the first minute". Sổ tay này đặt các điểm "re-engagement" (kéo người xem lại) quanh **phút thứ 3 và phút thứ 6** ([Netinfluencer](https://www.netinfluencer.com/mrbeast-productions-leaked-internal-document-rosanna-pansino/); [Gigazine](https://gigazine.net/gsc_news/en/20240917-mrbeast-youtube-production)). Paddy Galloway mở các tuyến truyện và đặt câu hỏi chưa trả lời trong khoảng **40 giây đầu** ([Scaleviews](https://scaleviews.beehiiv.com/p/how-paddy-galloway-forever-broke-the-youtube-algorithm)). Anh còn dùng một phép thử: 30 giây đầu của video dài có đứng riêng được như một Short không ([tóm tắt bài nói, nguồn thứ cấp](https://youtubesummary.com/summary/AX3dEGjBg6w)). Theo Galloway, đóng gói còn quan trọng hơn sản xuất: "The difference between a million views and 28 million views is how you package it". Creator hàng đầu dành khoảng **30% thời gian cho ý tưởng và đóng gói**, trong khi creator nhỏ chỉ dành khoảng 5% ([Colin and Samir](https://www.colinandsamir.com/resources/the-new-rules-of-youtube-from-paddy-galloway)).

Khung truyện chắc nhất đến từ Trey Parker và Matt Stone. Nếu giữa hai nhịp truyện điền được chữ "and then" (rồi thì) thì truyện nhạt. Các nhịp phải nối bằng **"therefore" (vì thế) hoặc "but" (nhưng)** ([Austin Kleon](https://tumblr.austinkleon.com/tagged/matt%20stone); [HuffPost UK](https://huffingtonpost.co.uk/entry/south-park-nyu_n_954419)). Thảm họa tự nhiên đã có sẵn chuỗi này: có cảnh báo băng, *nhưng* tàu vẫn giữ tốc độ; người gác thiếu ống nhòm, *vì thế* phát hiện băng quá muộn. Mỗi chữ "nhưng" là một lần móc người xem lại. Mẫu số 4 của Pixar ("Once upon a time… Every day… One day… Because of that… Until finally…") ([CUNY PDF](https://mes153stevenson.commons.gc.cuny.edu/files/2018/08/Pixars-22-Rules-of-Storytelling.pdf)) và vòng truyện 8 bước của Dan Harmon ([Arc Studio](https://www.arcstudiopro.com/blog/dan-harmons-story-circle-screenplay)) hợp khi bạn kể qua một con người cụ thể. Một mô hình ba lớp vòng lặp trên blog cũng đáng dùng. Lớp lớn là câu hỏi do tiêu đề tạo ra, giữ đến cuối. Lớp giữa là một câu hỏi cho mỗi đoạn. Lớp nhỏ là các móc cách nhau khoảng 6–20 giây. Blog này cảnh báo đừng mở quá nhiều vòng một lúc ([Autonolab](https://blog.autonolab.com/blog/2025-07-02-retention-engineering-hook-validation-loop-orchestration-and-pace-design/)). Lời khuyên "đổi nhịp mỗi 60–90 giây" cũng chỉ là lời khuyên trên blog; con số "+15–25% thời lượng xem" đi kèm không có nguồn ([OutlierKit](https://outlierkit.com/resources/youtube-hooks-and-retention/)).

Góc "câu chuyện chưa kể" nên lấy một người hoặc chi tiết **có thật, có tư liệu**, nằm bên trong sự kiện nổi tiếng. Ví dụ Titanic: thợ làm bánh trưởng Charles Joughin *khai rằng* ông ở dưới nước lạnh hơn hai giờ và cho rằng nhờ rượu mà sống sót. Ông khai trước Ủy ban điều tra Anh ngày 10/5/1912 ([Encyclopedia Titanica](https://www.encyclopedia-titanica.org/titanic-survivor/charles-john-joughin.html); [Wikipedia](https://en.wikipedia.org/wiki/Charles_Joughin)). Bài học ở đây: kể lời khai *như là lời khai*, không nói như sự thật đã được xác nhận. Về đạo đức, Archival Producers Alliance công bố bộ thực hành tốt về AI tạo sinh trong phim tài liệu (9/2024, được IDA ủng hộ). Bộ này cảnh báo AI có thể "muddies the historical record", và khuyên lập bảng kê mọi yếu tố AI, ghi công AI như ghi công tư liệu lưu trữ ([MIT Open DocLab](https://opendoclab.mit.edu/presents/archival-producers-alliance-apa-best-practices-use-generative-ai-documentaries/)). Kurzgesagt công khai một bảng nguồn cho mỗi video và viết khoảng **một chục bản nháp kịch bản** ([Kurzgesagt](https://kurzgesagt.org/youtube/)). Suy ra **(KN)**: người dẫn chuyện hư cấu dùng làm khung kể được, nếu bạn ghi rõ là nhân vật hư cấu. Nhưng không bao giờ đặt câu bịa vào miệng người thật.

Ngân sách chữ tính theo tốc độ đọc. Thoại kể chuyện thường đọc khoảng **150 từ/phút**, phim tài liệu **120–140**, nội dung chậm **110–130** ([IRPR](https://sounddesign.irpr.agency/tools/voiceover-word-count-calculator/)). Một người đọc chuyên nghiệp dùng khoảng **140 từ/phút** cho tài liệu dài, và hạ xuống **130** khi cần nhiều chỗ cho đồ họa ([Voicebros](https://voicebros.com/en/blog/voice-over-script-writing)). Tiếng Việt tính theo âm tiết nên con số sẽ khác. Hãy đo bằng cách thu thử 60 giây giọng TTS của chính bạn **(KN)**.

| Định dạng | Thời lượng | Số từ tiếng Anh (130–150 từ/phút) | Cấu trúc gợi ý (KN) |
|---|---|---|---|
| Short | 60–90 s | 140–225 từ | 1 người, 1 khoảnh khắc, 1 cú lật; câu cuối vòng về câu đầu |
| Long-form | 5 phút | ~700 từ | cold open → lời hứa → 3 đoạn → trả lời |
| Long-form | 7–10 phút | ~1.000–1.400 từ | cold open → 4–5 đoạn 60–90 s → móc lại ở ~3:00 và ~6:00 → trả lời ở 30–60 s cuối, không outro dài |

Shorts đã được dài tới **3 phút** từ 15/10/2024 ([PetaPixel](https://petapixel.com/2024/10/04/youtube-shorts-expands-video-length-to-three-minutes/)). Từ 31/3/2025, Short được tính một lượt xem mỗi khi bắt đầu chạy hoặc chạy lại ([Creator Essentials](https://www.creatoressentials.com/glossary/shorts-engaged-views/)). Các blog đặt mục tiêu "viewed" (người ở lại xem) 70–80%. Nhưng một kênh thật được dẫn trong bài chỉ đạt **26,6% viewed** so với 73,4% vuốt qua, nên đừng hoảng nếu số của bạn thấp ([Social Media Examiner](https://www.socialmediaexaminer.com/?p=251758)).

**Checklist kịch bản**

```
[ ] Tiêu đề tạo một câu hỏi lớn; cảnh mở đầu chứng minh lời hứa của tiêu đề trong ≤10–15 s (KN)
[ ] Không chào hỏi, không "đăng ký kênh" ở đầu
[ ] Câu đầu có một con số, giờ khắc hoặc tên người cụ thể (KN)
[ ] ~75 từ đầu (≈30 s) chứa đủ hook + lời hứa (KN, tính theo 150 từ/phút)
[ ] Đọc thử chuỗi nhịp: mỗi chỗ nối là "nhưng/vì thế", không phải "rồi thì"
[ ] Có điểm móc lại quanh phút 3 và phút 6 (theo sổ tay MrBeast)
[ ] Nhân vật "chưa kể" có thật, có tư liệu; lời khai được ghi là lời khai
[ ] Mỗi câu một ý, phần lớn câu 8–15 từ, mỗi nhịp một con số và gắn với hình (KN)
[ ] Chừa 10–15% thời lượng cho khoảng lặng, hình và âm thanh (KN)
[ ] Có bảng nguồn mô tả; ghi rõ nhân vật hư cấu và các cảnh dựng lại bằng AI
[ ] Kết thúc ngay sau khi trả lời câu hỏi lớn
```

## Người dẫn chuyện diễn bằng phản ứng, không bằng cử động nhiều

Thiết kế nhân vật phải qua được phép thử bóng dáng: tô đen toàn bộ hình mà vẫn nhận ra nhân vật ([3dsense](https://3dsense.net/blogs/shape-language-in-character-design-communicating-through-geometry)). Thứ tự làm là bóng dáng, rồi khóa màu, rồi mới thêm chi tiết ([RocketBrush](https://rocketbrush.com/blog/shape-language-in-game-character-design-how-to-make-characters-readable-and-consistent)). Quy ước nghề về hình khối: tròn là thân thiện, vuông là vững chãi, tam giác là nguy hiểm ([Binus DKV](https://binus.ac.id/bandung/dkv/2025/11/04/character-design-101-turning-simple-shapes-into-personality/)). Đây là quy ước của người làm nghề, không phải hiệu ứng tri giác đã được chứng minh. Với người dẫn chuyện cho đề tài bi kịch, chọn khối tròn pha vuông (đáng tin, vững) và tránh tam giác ở khối chính để khỏi trông như phản diện **(KN)**. Kiểm bóng dáng ở cỡ ảnh thu nhỏ và màn hình điện thoại, vì người dẫn thường chỉ chiếm một góc khung. Chưa tìm thấy nguồn đáng tin nào nói thư viện cần bao nhiêu biểu cảm. Gợi ý theo kinh nghiệm **(KN)**: bảng xoay 5 góc, khoảng 6 cảm xúc cơ bản cộng biến thể nhẹ, và 9–12 khẩu hình.

Phần diễn có nền chắc nhất là Ed Hooks. Ông nói: "Thinking tends to lead to conclusions, and emotion tends to lead to action" (suy nghĩ dẫn tới kết luận, cảm xúc dẫn tới hành động); "We humans empathize only with emotion" (con người chỉ đồng cảm với cảm xúc); "Acting is doing; acting is also reacting" (diễn là làm, và cũng là phản ứng); "Scenes begin in the middle" (cảnh bắt đầu từ giữa) ([Acting Coach Scotland](https://www.actingcoachscotland.co.uk/blog/principles-acting-animators-and-actors)). Theo Hooks, cảm xúc đứng một mình có "zero theatrical currency" (không có giá trị sân khấu); khán giả chỉ đồng cảm khi thấy nhân vật *làm* một việc và hiểu cảm xúc phía sau việc đó ([Ed Hooks](https://www.midnighteast.com/mag/?p=4216)). Áp vào người dẫn chuyện: lúc kể sự kiện thì ít cử chỉ. Lúc có cảm xúc (sốc, xót xa) mới có một hành động rõ: ngừng lại, cúi đầu, tay hạ xuống. Người dẫn quay sang nhìn hình lịch sử, giật mình hoặc im lặng sẽ sống hơn nhiều so với chỉ nói thẳng vào máy. Với nỗi buồn, người buồn thật thường thu mình và tránh gây chú ý ([Animation Mentor](https://animationmentor.com/blog/the-6-basic-emotions-animating-sadness-with-tim-ingersoll)). Vai sụp và đầu cúi gợi buồn, nhưng mặt buồn mà cổ cứng thì trông như máy ([Binus DKV](https://binus.ac.id/bandung/dkv/2025/11/03/building-emotion-through-movement-how-animators-make-you-feel/)). Sự tĩnh lặng là có chủ đích: ngừng ngắn tạo căng, ngừng dài gợi nội tâm ([StageMilk](https://www.stagemilk.com/?p=45414)).

Mắt là kênh mạnh nhất, và chớp mắt có số đo thật. Người bình thường chớp khoảng **17 lần/phút khi nghỉ, 26 lần khi trò chuyện, 4,5 lần khi đọc** ([Bentivoglio et al.](https://wicri-demo.istex.fr/Wicri/Sante/explor/MovDisordV3/Site/fr/Main/Exploration/bibRecord.php?hk=005409)). Một nghiên cứu khác đo khoảng 5 giây giữa hai lần chớp khi trò chuyện, tức khoảng 12 lần/phút ([ABO](https://www.aboonline.org.br/details/1605/en-US)). Max Planck đo chớp ngắn **208 ms** và chớp dài **607 ms**. Khi người nghe ảo chớp dài, người nói trả lời ngắn hơn mà không nhận ra ([Discover](https://www.discovermagazine.com/blinks-change-how-we-talk-to-each-other-1863)). Theo Bloop Animation, một cái chớp thường trong hoạt hình là **đóng 2 khung, giữ 1, mở 3**; chớp nhanh là đóng 2, mở 3, không giữ; chớp dài là đóng 3, giữ 2, mở 4. Liếc mắt khoảng 3 khung. Nên chớp khi quay đầu, khi nhân vật nhận ra điều gì, hoặc sau một cái nhìn lâu ([Bloop Animation](https://www.bloopanimation.com/blinking-animation/)). Disney Research cho thấy chớp mắt thật không đối xứng; luật "đóng và mở cùng số khung" làm mắt kém tự nhiên ([Disney Research](https://la.disneyresearch.com/wp-content/uploads/Modeling-and-Animating-Eye-Blinks-Paper.pdf)). Con số thực hành **(KN)**: người dẫn đang nói chớp mỗi 2–4 giây, đặt vào cuối câu hoặc lúc đổi ý; ở đoạn bi thương thì chớp chậm, thưa hơn và đầu cúi.

Khớp môi có công cụ miễn phí. Rhubarb Lip Sync có 6 khẩu hình cơ bản A–F cộng 3 khẩu hình mở rộng G, H và X (X là nghỉ). Công cụ nhận WAV/OGG, nên đưa kèm kịch bản bằng tùy chọn `-d`, và xuất ra JSON, TSV hoặc dat cho Moho/OpenToonz. Bộ nhận dạng mặc định chỉ hiểu tiếng Anh; chế độ `phonetic` dùng được cho mọi ngôn ngữ, kể cả tiếng Việt, nhưng kém chính xác hơn ([Rhubarb GitHub](https://github.com/DanielSWolf/rhubarb-lip-sync)). Adobe Character Animator dùng 11 khẩu hình cộng các khẩu hình lúc im lặng ([Adobe](https://www.adobe.com/learn/adobe-character-animator/web/lip-sync-mouth-shapes)). Về thời điểm: hàm mở **trước âm thanh 1–2 khung**, còn các âm B, M, P phải đóng miệng chính xác ([Pluralsight](https://www.pluralsight.com/resources/blog/software-development/proven-tips-animating-believable-lip-sync); [HighOnFilms](https://www.highonfilms.com/lip-sync-animation-techniques-every-character-animator-should-know/)). ElevenLabs trả mốc thời gian từng ký tự kèm audio ([ElevenLabs](https://elevenlabs.io/docs/api-reference/streaming-with-timestamps)). Azure Speech trả 22 viseme ID có mốc thời gian, hoặc 55 blend shape ở 60 fps. Chưa xác minh Azure có hỗ trợ tiếng Việt cho tính năng này ([Microsoft Learn](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/how-to-speech-synthesis-viseme)). Một bẫy hay gặp trong rig: đầu vào "smile" ở 100% đè hết khẩu hình. Biểu cảm phải là lớp cộng dồn (additive) ([Rive forum](https://rive.app/community/forums/support/fsnLLkXUaA62/blending-between-inputs/ftNEp8TkjtJb)).

Hoạt hình giản lược giúp một người làm nổi việc. Vẽ cách 2 khung (12 hình/giây ở 24 fps) là chuẩn hoạt hình truyền hình Mỹ; cách 3 khung (khoảng 8 hình/giây) hợp cảnh chậm ([iD Tech](https://www.idtech.com/blog/what-does-animating-on-ones-twos-and-threes-mean); [ANN](https://www.animenewsnetwork.com/encyclopedia/lexicon.php?id=61)). Hoạt hình giản lược kéo dài tư thế chính và dùng hình giữ ([GarageFarm](https://garagefarm.net/blog/limited-animation-what-is-it)). Mẹo **(KN)**: thân giữ nguyên tư thế, chỉ có mặt sống (chớp mắt, thở, đầu trôi nhẹ, môi chạy riêng). Máy đẩy chậm vào tranh tĩnh cho đoạn bi kịch, nơi ít chuyển động lại đúng tinh thần.

**Checklist người dẫn chuyện**

```
[ ] Bóng dáng nhận ra được ở cỡ ảnh thu nhỏ; khối chính tròn/vuông, không tam giác
[ ] Bảng xoay 5 góc + ~6 cảm xúc + 9 khẩu hình kiểu Rhubarb (KN)
[ ] Mỗi câu thoại ghi: đang "nghĩ" (ít cử động) hay "cảm" (một hành động rõ)
[ ] Mỗi đoạn có ít nhất một phản ứng với hình (nhìn sang, khựng lại, im lặng)
[ ] Chớp mắt có lý do (đổi ý, quay đầu, cuối câu); khoảng mỗi 2–4 s khi nói (KN)
[ ] Môi mở trước tiếng 1–2 khung; kiểm tay các âm M/B/P
[ ] Cảnh tang thương: giữ tư thế lâu, mắt nhìn xuống, chớp chậm, không khóc lóc cường điệu
[ ] Biểu cảm là lớp cộng dồn, không đè khẩu hình
```

**Từ khóa diễn cho prompt video AI (tiếng Anh)**

```
Narrator acting keys: "listens, then reacts", "small head tilt", "glances toward the image",
"brief pause before speaking", "shoulders drop slightly", "eyes lower, slow blink",
"restrained grief, no tears", "holds still for a beat", "hand gesture opens toward the map",
"wry half-smile" (light topics only), "speaks to camera, calm, measured pace"
Avoid: "exaggerated crying", "wild gestures", "constant movement", "shouting"
```

## Hình ảnh: cảm xúc đứng trên không gian, màu đi theo đường cảm xúc

Thước đo khi chọn cú cắt là "luật sáu" của Walter Murch, xếp theo trọng số: **cảm xúc 51%, truyện 23%, nhịp 10%, đường mắt 7%, mặt phẳng 2D 5%, không gian 3D 4%**. Khi buộc phải hy sinh, bỏ từ dưới lên ([FilmDaft](https://filmdaft.com/walter-murchs-rule-of-six-the-editors-formula-for-choosing-the-right-cut/); [No Film School](https://nofilmschool.com/2016/11/6-rules-good-cutting-according-oscar-winning-editor-walter-murch)). Các phần trăm này chỉ để xếp thứ tự, không phải công thức. Luật 180 độ giữ quan hệ trái/phải giữa các nhân vật. Được phá luật, nhưng phải có chủ ý ([StudioBinder](https://www.studiobinder.com/blog/what-is-the-180-degree-rule/)). Khi cắt giữa hai người nhìn nhau, khớp cỡ cảnh, khoảng cách, tiêu cự và đường chân trời ([StudioBinder](https://www.studiobinder.com/blog/what-is-an-eyeline-match/)). Video AI hay "quên" máy đang ở đâu giữa các shot, nên mỗi shot cần ghi hướng màn hình ([HackerNoon](https://hackernoon.com/ai-video-generation-forgets-where-the-camera-was-heres-the-screen-direction-workflow-that-fixes-it)). Bruce Block đưa ra nguyên lý **tương phản và tương đồng** trên bảy thành phần: không gian, đường nét, hình khối, sắc độ, màu, chuyển động, nhịp ([O'Reilly](https://www.oreilly.com/library/view/the-visual-story/9781317745693/xhtml/Ch02.xhtml)). Áp vào truyện thảm họa: đoạn bình yên giữ tương đồng (ít tương phản), cao trào đẩy tương phản lên mạnh nhất.

Máy quay 2D/2.5D dựa trên nguyên lý của máy multiplane: lớp càng xa thì chạy càng chậm. Cho lớp trước và lớp sau chạy ngược chiều thì tạo được cảm giác xoay ([Wikipedia](https://en.wikipedia.org/wiki/Multiplane_camera)). Hiệu ứng Ken Burns phải nhẹ, có ease đầu và cuối, tốc độ theo độ dài clip, và không lặp cùng một kiểu chuyển động ([Larry Jordan](https://larryjordan.com/articles/final-cut-pro-x-create-a-ken-burns-effect/); [WeVideo](https://awstest.wevideo.com/blog/for-work/being-ken-burns-test)). Push-in chậm dùng cho khoảnh khắc nhận ra và đau buồn; push-in nhanh dùng cho sốc. Nguồn cho ý này mỏng, chỉ là một glossary ([Morphic](https://morphic.com/ai-glossary/push-in)). Vox render một số đồ họa ở 12 fps trong bản dựng 24 fps để có cảm giác giật kiểu stop-motion ([PremiumBeat](https://www.premiumbeat.com/blog/replicating-vox-motion-graphic/)). Không có nguồn nào cho số chuẩn về tốc độ zoom, đường cong easing hay tỷ lệ tốc độ giữa các lớp parallax. Bảng dưới là điểm xuất phát **(KN)**, cần thử bằng mắt.

| Thông số (KN) | Đoạn kể thường | Đoạn căng/va chạm | Đoạn bi kịch/suy ngẫm |
|---|---|---|---|
| Độ dài shot | 3–6 s | 1–3 s | 6–12 s |
| Máy | trượt/parallax 3–5 lớp, có ease | push nhanh, rung nhẹ, whip pan | push-in rất chậm hoặc đứng yên |
| Chuyển cảnh | cắt thẳng, match cut | cắt gấp, impact ở khung đầu | dissolve chậm, L cut |
| Khoảng lặng | — | 0,5–2 s trước impact | 2–4 s không lời ở khoảnh khắc đỉnh |

Các con số nhịp trong bảng dựa trên dữ liệu điện ảnh thật. Độ dài shot trung bình của phim Mỹ khoảng **10 giây ở thập niên 1930–1940, xuống dưới 4 giây sau năm 2000**. Shot ngắn thì đi kèm nhiều chuyển động trong khung hơn (r = −0,46) ([Cutting et al., PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3485803/)). Với YouTube, blog của các hãng khuyên đổi một yếu tố hình mỗi **10–15 giây** ở phần mở ([Pixflow](https://pixflow.net/blog/?p=93140)) hoặc **15–25 giây** với khán giả trẻ. Khán giả trên 25 tuổi hợp nhịp cắt chậm hơn, và "overediting here actually decreases retention" (dựng quá tay làm giảm giữ chân) ([AIR Media-Tech](https://air.io/en/youtube-hacks/advanced-retention-editing-cutting-patterns-that-keep-viewers-past-minute-8)). Một cảnh báo đáng nhớ: "constant zooms, captions, sound hits, and stock overlays can create activity without meaning" (zoom, chữ, tiếng đập và lớp phủ liên tục tạo ra cảm giác bận rộn mà không có ý nghĩa) ([CapCut/Dreamina](https://dreamina.capcut.com/ai-video/youtube-audience-retention)). Chưa ai đo độ dài shot trung bình của kênh tài liệu hoạt hình YouTube. Nếu muốn biết, phải tự đo trên kênh mẫu.

Chuyển cảnh nên mang ý nghĩa. Match cut đồ họa nối hai khoảnh khắc bằng cùng hình khối, màu hoặc bố cục, như cục xương thành tàu vũ trụ trong *2001* ([StudioBinder](https://www.studiobinder.com/blog/match-cuts-creative-transitions-examples/); [FilmDaft](https://filmdaft.com/?p=36584)). Với Titanic, ví dụ là con tàu lúc hạ thủy chuyển thành xác tàu dưới đáy biển, cùng vị trí trong khung. J cut (âm cảnh sau vào trước hình) và L cut (âm cảnh trước kéo dài sang hình sau) là công cụ chuẩn của phim tài liệu ([Wikipedia](https://en.wikipedia.org/wiki/J_cut)). Kurzgesagt chọn một **ẩn dụ hình ảnh cho từng cảnh ngay ở bước phác**, và để bản lời đã thu quyết định nhịp hoạt hình ([Kurzgesagt](https://kurzgesagt.org/youtube/)). Số liệu nên gắn vào hình cụ thể. Ví dụ **(KN)**: mỗi người một chấm, và thuyền cứu sinh lấp dần, thay cho biểu đồ cột. Bản đồ kiểu Johnny Harris thường làm bằng After Effects với plugin GEOlayers, Google Earth Studio và Mapbox ([aescripts](https://aescripts.com/learn/making-maps-for-johnny-harris---volcanoes/); [PremiumBeat](https://www.premiumbeat.com/blog/making-maps-for-johnny-harris/)). Vox giao riêng cho một người trong đội việc kiểm độ chính xác của bản đồ ([Storybench](https://www.storybench.org/?p=21229)).

Color script của Pixar bắt đầu từ Ralph Eggleston trong *Toy Story*: một dải tranh nhỏ vẽ toàn phim. Màu đậm lên khi cảm xúc mạnh và dịu đi ở khoảnh khắc u buồn; sau đó Pixar làm color script cho mọi phim ([MoMA](https://www.moma.org/audio/playlist/192/2581); [Hyperallergic](https://hyperallergic.com/610771/the-art-of-pixar-chronicle-books/)). Màu nhạt và xám làm thế giới cảm xúc trông "drained" (cạn kiệt) ([Fiveable](https://fiveable.me/film-and-media-theory/key-terms/color-grading)). Nhưng xám dùng như mặc định bất kể câu chuyện thì bị chê là nhàm ([Goldsmiths](https://mccs-journalism.gold.ac.uk/wp/pacmag/?p=973)). Một điểm đáng chú ý: phim nói chung tối dần qua các thập niên, còn hoạt hình vẫn giữ sáng ([Cutting et al.](https://pmc.ncbi.nlm.nih.gov/articles/PMC3485803/)). Vì vậy kênh hoạt hình không cần tối thui mới thành bi kịch; giảm bão hòa phải có lý do theo truyện.

**Color script mẫu cho một tập thảm họa (KN)**

| Đoạn | Màu chủ đạo | Bão hòa | Ấm/lạnh | Tương phản |
|---|---|---|---|---|
| Mở đầu, hy vọng | vàng kem, đồng | vừa | ấm | thấp |
| Đêm, dấu hiệu nguy hiểm | xanh đêm | vừa–thấp | lạnh | tăng dần |
| Cao trào | đen + điểm sáng đèn/pháo sáng | chọn lọc | lạnh, điểm nóng | cao nhất |
| Sau thảm họa | xám xanh | thấp | lạnh | thấp |
| Kết | xám + một vật giữ màu ấm | chọn lọc | ấm ở một điểm | thấp |

Với chủ đề nhẹ (phát minh, chuyện lạ), giữ màu bão hòa cao, tương phản vừa, nhịp nhanh hơn, và cho người dẫn có những cử chỉ hài khô.

**Từ khóa hình ảnh cho prompt AI (tiếng Anh)**

```
Tragedy: "muted desaturated palette, cold blue-grey night, single warm light source,
low contrast aftermath, slow push-in, static wide shot of vast dark ocean, small human figures
for scale, stillness, respectful distance, no gore, no visible bodies"
Tension: "rising contrast, dutch angle only at panic, flickering deck lights, tight close-up,
quick cut, handheld micro-shake"
Light topic: "warm saturated flat 2D, clean shapes, playful timing, bright soft daylight"
Continuity: "keep screen direction: ship moves left to right", "camera stays on the same side of
the line", "same framing as previous shot"
```

## Âm thanh: nhạc thảm họa sống bằng kết cấu, lời dẫn sống nhờ nhạc nhường chỗ

Nhạc thảm họa hiện đại đáng sợ vì kết cấu chứ không vì giai điệu. Hildur Guðnadóttir làm toàn bộ âm thanh cho nhạc phim *Chernobyl* từ bản thu tại một nhà máy điện hạt nhân đã ngừng ở Litva. Cách làm này tránh hẳn khuôn sáo kiểu tiếng máy đếm Geiger: "most of it is about listening" (phần lớn là lắng nghe) ([CDM](https://cdm.link/chernobyl-score-hildur-gudnadottir/); [Grapevine](https://grapevine.is/?p=10008962)). *Dunkirk* dùng Shepard tone, ảo giác cao độ dâng mãi mà không bao giờ lên tới đỉnh. Nolan còn gửi bản thu tiếng đồng hồ của mình để Zimmer làm thành nhịp tích tắc xuyên phim ([Kottke](https://kottke.org/18/05/hans-zimmers-clever-use-of-the-shepard-scale-in-dunkirk); [Classic FM](https://www.classicfm.com/composers/zimmer/music/christopher-nolan-interview/)). Với *Sicario*, Villeneuve yêu cầu "music you can feel as much as you can hear" (nhạc cảm thấy được nhiều như nghe thấy) ([Screen Daily](https://screendaily.com/awards/composers-johann-johannsson-sicario/5098958.article)). Jóhannsson đáp bằng trống tom trầm đập như "heartbeat" (nhịp tim) và dây trầm trượt xuống ([MovieMom](https://moviemom.com/interview-johann-johannsson-composer-of-sicario/); [Orchestration Online](https://orchestrationonline.com/2016-oscars-orchestration-review-johann-johannssons-sicario/)). Về sự tôn trọng: Kerry Muzzey nói nhạc tài liệu "has to be very scaled back" (phải tiết chế rất nhiều) để khỏi thao túng người xem ([motionpictures.org](https://www.motionpictures.org/2015/11/composer-kerry-muzzey-scoring-intimate-doc-seer/)). Earl Rose bỏ nhạc hoàn toàn khi nhân vật đang nói ([Variety](https://variety.com/2009/film/markets-festivals/documentary-scoring-requires-fine-balance-1118007649)). Suy ra **(KN)**: ngay khoảnh khắc có người chết, đừng dùng nhạc "epic trailer". Dùng một drone mỏng, hoặc im lặng.

Hoạt hình không có âm thanh gốc, nên mọi lớp phải tự dựng. Thứ tự lớp là thoại, foley, ambience, nhạc, rồi mix cuối ([IRPR](https://sounddesign.irpr.agency/guides/how-to-mix-audio-for-youtube/)). Tiếng impact nghe nặng nhờ **khoảng lặng ngay trước nó**, không nhờ âm lượng ([IRPR](https://sounddesign.irpr.agency/guides/how-to-add-weight-to-impacts/)). Mẹo **(KN)**: hạ nhạc và ambience xuống rất nhỏ trong 0,5–2 giây trước cú va chạm, nhưng giữ lại một tiếng nhỏ (tiếng thở, tích tắc) để người xem biết đó là cố ý, không phải lỗi. Riser kết thúc đúng khung cắt; impact đặt ở khung đầu tiên của hình mới. Âm thanh phóng đại (whoosh, sub boom) hợp đoạn infographic, nhưng nên giảm ở khoảnh khắc có người chết.

Mix lời dẫn có các con số khá thống nhất giữa các nguồn, dù phần lớn là nguồn của hãng plugin và blog. Nhạc nằm thấp hơn giọng **12–18 dB** ([Sonilo](https://sonilo.com/blog/how-to-add-background-music-to-a-video)) hoặc **15–20 dB** khi có lời ([IRPR](https://sounddesign.irpr.agency/guides/how-to-mix-audio-for-youtube/)). Lemo-Opuscar để giọng cao hơn nhạc khoảng **10 dB** ([TECHNIQUE.md](https://raw.githubusercontent.com/lemomo-ai/lemo-opuscar/main/TECHNIQUE.md)). Thông số sidechain ducking: attack **1–10 ms**, release **500–1.500 ms**, tỷ lệ 4:1, giảm 6–12 dB (mức nhẹ) tới khoảng 20 dB (mức mạnh). Attack dài làm lọt đầu chữ; release ngắn làm nhạc "bơm" lên xuống ([Vindral](https://composer-docs.vindral.com/script-objects/script-objects-operators-sidechain-ducking.html)). EQ động khoét chỗ cho thoại trên bus nhạc ([ProSoundWeb/iZotope](https://www.prosoundweb.com/izotope-releases-rx-final-mix/)). Vùng xì (sibilance) thường ở **5–8 kHz** ([IRPR](https://sounddesign.irpr.agency/glossary/de-esser/)). Netflix chuẩn hóa theo thoại: **−27 LKFS ±2 LU, true peak ≤ −2 dBTP** ([Netflix](https://backlothelp.netflix.com/hc/en-us/articles/360001794307-Netflix-Sound-Mix-Specifications-Best-Practices-v1-5)). YouTube chuẩn hóa khi phát về khoảng **−14 LUFS** và chỉ hạ, không nâng: video ở −10 LUFS sẽ bị hạ 4 dB ([Wikipedia](https://en.wikipedia.org/wiki/Audio_normalization); [MeterPlugs](https://meterplugs.com/blog/2019/09/18/youtube-changes-loudness-reference-to-14-lufs.html)). Mức xuất khuyến nghị là true peak −1 dBTP ([Youlean](https://youlean.co/?p=30813)). YouTube không công bố mức chuẩn này chính thức ([Videvo](https://videvo.net/blog/?p=40770)). Loa điện thoại mất nhiều ở dưới khoảng 500 Hz và trên 6 kHz ([SoundGirls](https://soundgirls.org/lost-in-translation/)). Phần dưới 120–150 Hz nên giữ ở giữa (mono) ([Violet Recording](https://violetrecording.com/how-to-check-mono-compatibility/)).

**Công thức mix khởi điểm cho lời dẫn TTS**

| Bước | Thông số | Loại |
|---|---|---|
| High-pass giọng | 80–100 Hz | KN |
| De-ess split-band | 5–8 kHz, giảm 3–6 dB | dải có nguồn, mức giảm là KN |
| Nén giọng TTS | 2:1–3:1, giảm 3–6 dB (TTS vốn đều, nên nén ít) | KN |
| Nhạc dưới giọng | 12–20 dB | có nguồn (blog/hãng) |
| Ducking | attack 1–10 ms, release 500–1.500 ms, 4:1, giảm 8–15 dB | có nguồn (tài liệu hãng); mức 8–15 dB là KN |
| EQ động trên nhạc | cắt 3–6 dB quanh 1–4 kHz khi có lời | KN; các nguồn chưa thống nhất dải tần |
| Lời dẫn short-term | khoảng −16 đến −18 LUFS | KN (quy đổi) |
| Master | −14 LUFS integrated ±1, true peak −1 dBTP (−2 nếu còn nén lại sang AAC) | có nguồn (không chính thức) |
| Kiểm tra | loa điện thoại + mono; drone dưới 60 Hz thêm hài âm 100–200 Hz | có nguồn / KN |

CapCut, Premiere và DaVinci đều có auto-ducking ([Sonilo](https://sonilo.com/blog/how-to-add-background-music-to-a-video)). Trong pipeline code, bạn đã biết sẵn mốc lời từ file timing của TTS, nên có thể hạ gain nhạc theo một đường cong vẽ trước thay vì dùng compressor **(KN)**.

**Từ khóa nhạc và âm thanh cho AI (tiếng Anh)**

Mẹo cộng đồng Suno: chọn dòng nhạc hẹp, tả nhạc thay đổi theo thời gian, xếp prompt theo lớp (kết cấu, hòa âm, nhạc cụ, cảm xúc), và tránh từ mơ hồ như "professional" ([Jack Righteous](https://jackrighteous.com/fr/blogs/guides-using-suno-ai-music-creation/what-is-cinematic-music-suno-ai-guide); [HookGenius](https://hookgenius.app/suno-cheat-sheet/)). Đây không phải tài liệu chính thức của Suno.

```
Disaster underscore: "dark ambient documentary underscore, low cello drone, slow sub pulse like a
heartbeat, descending low-string glissando, metallic industrial textures, distant ship horn,
sparse, no melody, no drums until the final third, slowly building tension, stays minimal under
narration, instrumental, no vocals"

Countdown / rising dread: "ticking clock ostinato, endless Shepard-tone riser, low tom heartbeat,
unresolved minor-second clusters, tension without release"

Loss / aftermath (respectful): "solo felt piano, very sparse, long silences, soft room reverb,
cold strings pad, restrained, no swell, no epic percussion"

Light topic host theme: "playful pizzicato strings, light marimba, curious and warm,
mid-tempo, clean, leaves space for voice-over"

Always add: "instrumental, no lead melody in the vocal range, leaves space for narration"

SFX list (Titanic): "deep hull groan, ice scraping steel, distant crowd murmur, water rushing
into corridor, rope creak, lifeboat pulley, flare whoosh and pop, silence with faint wind"
```

## Kênh lớn giữ cố định giọng và nét vẽ, và chỗ trống cho người dẫn hiện hình

Có hai mô hình đã chứng minh được hiệu quả. Mô hình thứ nhất là một tác giả làm gần hết, ra video thưa nhưng có giọng kể rất riêng. OverSimplified có video dài 10–20 phút và ra cực thưa: tập đầu tháng 10/2016, một tập năm 2025 ([fandom](https://oversimplified.fandom.com/wiki/List_of_OverSimplified_episodes); [The Central Trend](https://thecentraltrend.com/126092/opinion/oversimplified-really-knows-how-to-make-history-fun/)). LEMMiNO tự công bố bộ công cụ After Effects, Cinema 4D, Blender, Unreal, Audition, FL Studio/Ableton, và tự làm một phần nhạc ([LEMMiNO FAQ](https://www.lemmi.no/faq)). Ở Việt Nam, Dòng Máu Việt do một người làm bằng điện thoại và máy tính cũ, video dưới 1 phút, đạt khoảng **1,35 triệu theo dõi và hơn 750 triệu lượt xem YouTube**. Đổi lại, kênh bị khóa nhiều lần vì hình ảnh chiến tranh ([Thanh Giong](https://thanhgiong.vn/nhung-nguoi-tre-lam-clip-lich-su-trieu-view-58409.html)). Mô hình thứ hai là studio. Kurzgesagt có khoảng **70 người** và hơn 25 triệu người đăng ký ([Wikipedia](https://en.wikipedia.org/wiki/Kurzgesagt)). Mỗi video tốn ít nhất khoảng **1.200 giờ công**, và nhóm làm song song 2–4 video ở các khâu khác nhau ([VoiceTube](https://voicetube.com/videos/123700)). Simple History đạt gần 5 triệu người đăng ký và khoảng 20 triệu lượt xem mỗi tháng, rồi nhận khoản đầu tư bảy chữ số năm 2024 ([Tubefilter](https://www.tubefilter.com/2024/04/16/simple-history-electrify-video-partners-investment/)). EZ Sử có nhóm 9 người; video đầu mất khoảng 3 tháng; video 21 phút đạt khoảng 13 triệu lượt xem ([Thanh Giong](https://thanhgiong.vn/nhung-nguoi-tre-lam-clip-lich-su-trieu-view-58409.html)). TED-Ed theo dây chuyền: kịch bản khoảng **800–900 từ** cho bài học khoảng 5 phút, có storyboard trước khi thu lời ([Amara](https://amara.org/videos/UWTssHkaY2kO/tr/3045470/)).

Sự nhất quán của các kênh này đứng trên ba trụ. Trụ thứ nhất là **một giọng cố định nhiều năm**: Steve Taylor đọc cho Kurzgesagt từ video đầu tiên, Josh Risser đọc cho The Infographics Show ([Wikipedia](https://en.wikipedia.org/wiki/Kurzgesagt); [Sportskeeda](https://wiki.sportskeeda.com/youtube/the-infographics-show)). Trụ thứ hai là **bản sắc âm nhạc**: Kurzgesagt soạn nhạc gốc theo video đã dựng, LEMMiNO tự làm nhạc. Trụ thứ ba là **nét vẽ đủ riêng để thị trường gọi tên**: đã có tin tuyển "Animator in the Style of Simple History" và dịch vụ "Zack D Films style" trên Fiverr ([OnlineJobs.ph](https://www.onlinejobs.ph/jobseekers/job/1213465); [Fiverr](https://fiverr.com/leafxstudio/create-short-3d-animations-like-zack-d-films)). Không kênh nào công bố style guide nội bộ. Điểm quan trọng cho bạn: trong mẫu khảo sát **không có kênh lớn nào dùng người dẫn hoạt hình hiện hình cố định**. Người dẫn hiện hình vì vậy có thể là bản sắc riêng của kênh bạn, nhưng là bản sắc chưa được kiểm chứng. Hãy coi nó là giả thuyết, và đo bằng chỉ số Intro cùng điểm rơi trên biểu đồ giữ chân **(KN)**.

Chính sách YouTube là ràng buộc cứng. Từ **15/7/2025**, chính sách "repetitious content" đổi tên thành "inauthentic content". Bị nhắm là các truyện kể gần như giống nhau, slideshow chung một lời đọc, video theo khuôn ít khác biệt, đăng số lượng lớn. AI không bị cấm nếu sản phẩm cuối là nội dung gốc và có giá trị ([Search Engine Journal](https://www.searchenginejournal.com/youtube-monetization-update-spam-not-reaction-channels/550755/)). Về nhãn nội dung tổng hợp: phải khai khi nội dung *trông như thật*, ví dụ người thật nói điều chưa từng nói, hoặc cảnh thực tế chưa từng xảy ra. Nội dung không thực tế "such as animation" thì không bắt buộc khai, và khai cũng không làm giảm phân phối ([YouTube Help](https://support.google.com/youtube/answer/14328491)). Nguyên tắc nội dung thân thiện với nhà quảng cáo vẫn cho quảng cáo đầy đủ với nội dung lịch sử hoặc giáo dục về thảm kịch, nếu ít hoặc không chiếu bạo lực và không "exploitative" (khai thác). Mô tả chi tiết ghê rợn bị hạn chế quảng cáo. Cảnh thương vong ghê rợn trong chiến tranh thì không được quảng cáo "in any context" (trong bất kỳ bối cảnh nào) ([YouTube Help](https://support.google.com/youtube/answer/6162278)).

**Checklist phong cách kênh**

```
[ ] Một giọng người dẫn duy nhất (giọng mẫu cố định), không đổi giữa các tập
[ ] Một nhân vật dẫn với bảng xoay + bộ biểu cảm khóa; xuất hiện ở vị trí cố định: mở tập,
    chuyển đoạn, kết (KN)
[ ] Một bảng màu kênh + color script riêng cho từng tập
[ ] Một chủ đề nhạc 3–5 s (logo âm thanh) + bảng từ khóa nhạc theo mood (KN)
[ ] Một kiểu chữ, một kiểu bản đồ, một kiểu đồ họa số liệu
[ ] Mỗi tập: góc nhìn riêng, nghiên cứu riêng, bảng nguồn — bằng chứng "authentic"
[ ] Thảm họa: không chiếu khoảnh khắc chết, không gore, tiêu đề/ảnh thu nhỏ không câu view
    bằng bi kịch
[ ] Cảnh trông như ảnh thật về người/sự kiện thật → bật nhãn nội dung tổng hợp
[ ] Làm song song 2–4 tập ở các khâu khác nhau để giữ nhịp đăng
[ ] Short = trailer cho tập dài, cùng người dẫn
```

## Seedance cho phần diễn, code cho phần thông tin

Lemo-Opuscar là bộ skill cho Claude Code, làm phim ngắn "without a video model" (không dùng model video). Bộ có 51 phong cách; mọi phim mẫu đều do agent viết code đạo diễn, vẽ, soạn nhạc và hòa âm. Mặc định xuất 1920×1080 ở 24 fps, mỗi phim mất **khoảng 30–60 phút**, và tác giả nói các phong cách được tinh chỉnh cho Claude Opus 5.5 ([GitHub](https://github.com/lemomo-ai/lemo-opuscar)). Về kỹ thuật, mỗi phim là một trang web có hàm `render(t)` tất định, chạy trong Chrome không giao diện. Canvas 2D lo phần 2D, three.js lo phần 3D, shader WebGL2 lo hậu kỳ. Âm thanh được chuẩn hóa loudnorm hai lượt về **−14 LUFS**. Giọng dùng Kokoro (tiếng Anh) và faster-whisper để kiểm thoại cùng lấy mốc từng từ. `timeline.js` là nguồn nhịp duy nhất, và `cuecheck.py` kiểm độ lệch hình–nhạc với mục tiêu 0 ms ([TECHNIQUE.md](https://raw.githubusercontent.com/lemomo-ai/lemo-opuscar/main/TECHNIQUE.md)). Giới hạn quan trọng nhất là ở nhân vật: rig 2.5D chỉ "enough for pantomime" (đủ cho kịch câm), và tài liệu không mô tả cách khớp môi (cùng nguồn). Lip sync tiếng Việt bằng code làm được ở mức gần đúng: Rhubarb ở chế độ `phonetic`, hoặc lấy mốc từ của whisper rồi ánh xạ sang miệng đóng/mở.

Video AI thì diễn giỏi hơn hẳn nhưng khó kiểm soát. Theo review thực tế, Seedance 2.0 khóa ref giữ được mặt và trang phục, nhưng thoại dài thỉnh thoảng có tạp âm và take dài dễ vỡ khi vật lý phức tạp ([Magic Hour](https://magichour.ai/blog/seedance-20-review)). Theo nguồn bên thứ ba (chưa thấy thông báo chính thức của ByteDance), Seedance 2.5 gen tối đa **30 giây** mỗi lần, nhận tối đa **50 ref** (30 ảnh, 10 video, 10 audio), gen hình và tiếng trong cùng một lượt, và lúc ra mắt chỉ có 480p/720p ([PixVerse](https://pixverse.ai/en/blog/seedance-2-5-vs-seedance-2-0); [Morphic](https://morphic.com/resources/how-to/seedance-2-5-guide)). Ref audio cho phép gắn giọng mẫu của người dẫn, để giọng đồng nhất qua mọi tập. Chưa có nguồn chính thức nào xác nhận lip sync tiếng Việt cho Seedance, Kling hay Veo. Hãy thử một take ngắn trước khi chốt ngôn ngữ thoại cho kênh. Về giá niêm yết (bên thứ ba): Sora 2 720p khoảng $0,10/s ([CometAPI](https://www.cometapi.com/sora-api-access-in-2026-pricing-rate-limits-and-what-s-actually-available-through-aggregators/)); Veo 3.1 khoảng $0,40/s, bản Lite $0,05/s ([benchlm](https://benchlm.ai/media-pricing/veo)); Kling 3.0 Turbo ¥0,8/s ở 720p ([Atlas Cloud](https://www.atlascloud.ai/blog/guides/kling-3.0-turbo-kling-omni)). Một phút thành phẩm vì thế tốn khoảng **$6–24**, chưa tính gen lại. Giá Seedance qua Magnific thì phải xem bằng `simulate_cost`. Về TTS, ElevenLabs có tiếng Việt ở v4, v4 Turbo, v3 và Flash v2.5, nhưng không có ở Multilingual v2. Bản v3 điều khiển cảm xúc bằng tag như `[sad]` và `[whispers]`, nhưng là bản thử nghiệm; tài liệu khuyên dùng v4 cho việc mới ([ElevenLabs](https://elevenlabs.io/docs/overview/models)).

| Tiêu chí | Code (Claude Code + canvas/WebGL, Lemo-Opuscar) | AI video (Seedance qua Magnific) |
|---|---|---|
| Nhân vật đồng nhất | tuyệt đối | tốt, vẫn còn trôi |
| Diễn mặt và thân | thấp: kịch câm, khẩu hình rời | cao, gần điện ảnh |
| Khớp môi | viseme/Rhubarb; tiếng Việt gần đúng | gen cùng hình; tiếng Việt chưa xác nhận |
| Máy quay, bản đồ, số liệu, chữ | chính xác từng pixel | theo xác suất, chữ dễ sai |
| Sửa một chi tiết | sửa một dòng rồi render lại | gen lại cả take |
| Chi phí | gần như chỉ token + thời gian máy | khoảng $6–24/phút niêm yết (bên thứ ba) |
| Khớp nhạc | 0 ms theo timeline | dựng lại trong CapCut |

Từ bảng này, pipeline đề xuất **(KN)** cho một người làm như sau. Kịch bản và bảng nguồn đi trước. Thu lời dẫn bằng giọng mẫu cố định trước khi làm hình, giống Kurzgesagt và TED-Ed. Cảnh người dẫn diễn và nói, cùng các cảnh tái hiện có người, đi qua Seedance với ref nhân vật và ref audio giọng mẫu, take 10–15 giây. Bản đồ hành trình, đồng hồ đếm ngược, số liệu (chấm người, thuyền cứu sinh lấp dần), tiêu đề chương, mở đầu và kết thúc đi qua nhánh code. Nhánh này rẻ, đồng nhất, và khớp mốc lời đến từng mili giây. Nhạc nền cho các đoạn thông tin có thể sinh bằng code: Shepard riser và drone viết bằng numpy rất dễ. CapCut ghép tất cả, auto-duck nhạc theo lời, rồi xuất −14 LUFS. Để hai nhánh trông như cùng một phim, khóa chung bảng màu, kiểu chữ và hạt phim: thêm grain bằng ffmpeg cho cả clip AI lẫn clip code.

**Checklist pipeline**

```
[ ] Kịch bản + bảng nguồn + ghi chú "ẩn dụ hình" cho từng đoạn trước khi gen
[ ] Lời dẫn thu trước; lấy mốc từ (faster-whisper / ElevenLabs timestamps)
[ ] Gắn nhãn từng shot: DIỄN (Seedance) hay THÔNG TIN (code)
[ ] Shot Seedance: ref nhân vật + giọng mẫu ở cổng audio + hướng màn hình ghi rõ
[ ] Thử lip sync tiếng Việt trên 1 take ngắn trước khi chốt ngôn ngữ thoại
[ ] Shot code: render(t) tất định, 24 fps, cùng bảng màu/kiểu chữ kênh
[ ] Grain/LUT chung cho cả hai nhánh
[ ] CapCut: J/L cut ở chỗ chuyển đoạn, auto-duck, xuất −14 LUFS / −1 dBTP
[ ] Nghe trên loa điện thoại và ở mono trước khi đăng
[ ] Sau khi đăng: đọc Intro 30 s và các điểm rơi, so với 10 video cùng độ dài
```

## Bảng tách số có nguồn và số kinh nghiệm

| Con số | Giá trị | Trạng thái |
|---|---|---|
| Chỉ số Intro của YouTube | % còn xem sau 30 s | có nguồn (YouTube) |
| "Above typical intro" | ≥50% sau 30 s | bên thứ ba, chưa kiểm |
| Điểm móc lại | phút 3 và phút 6 | có nguồn (sổ tay MrBeast bị lộ) |
| Đổi nhịp | 60–90 s; vòng nhỏ 6–20 s | blog |
| Tốc độ đọc | 130–150 từ/phút (tài liệu 120–140) | có nguồn (blog nghề) |
| Kịch bản TED-Ed | 800–900 từ | có nguồn |
| Shorts tối đa | 3 phút (từ 15/10/2024) | có nguồn |
| Độ dài shot trung bình phim Mỹ | ~10 s (1930s) → <4 s (sau 2000) | có nguồn (nghiên cứu) |
| Đổi yếu tố hình trên YouTube | 10–15 s hoặc 15–25 s | blog hãng |
| Độ dài shot theo đoạn | 3–6 / 1–3 / 6–12 s | KN |
| Chớp mắt | 17/phút khi nghỉ, 26/phút khi nói; 208/607 ms | có nguồn (nghiên cứu) |
| Khung chớp mắt | 2–1–3 khung | có nguồn (Bloop) |
| Môi mở sớm | 1–2 khung | có nguồn (blog nghề) |
| Vẽ cách 2 / cách 3 khung | 12 / ~8 hình/giây | có nguồn |
| Luật Murch | 51/23/10/7/5/4 % | có nguồn (sách, qua bài tóm tắt) |
| Nhạc dưới giọng | 12–20 dB (Lemo-Opuscar ~10 dB) | có nguồn (blog/hãng) |
| Ducking | attack 1–10 ms, release 500–1.500 ms, 4:1 | có nguồn (tài liệu hãng) |
| De-ess | 5–8 kHz | có nguồn |
| Netflix theo thoại | −27 LKFS ±2, −2 dBTP | có nguồn (chính thức) |
| YouTube | ~−14 LUFS, −1 dBTP | có nguồn, YouTube không công bố |
| Im lặng trước impact | 0,5–2 s | KN |
| J cut lead | 0,5–1,5 s | KN |
| Lời dẫn short-term | −16 đến −18 LUFS | KN |
| Kurzgesagt | ≥1.200 giờ/video, ~70 người | có nguồn |
| Lemo-Opuscar | 30–60 phút/phim, 24 fps, −14 LUFS | có nguồn (repo) |
| Seedance 2.5 | 30 s, 50 ref, 720p | bên thứ ba |
| Giá AI video | $6–24/phút thành phẩm | bên thứ ba + tính toán |

## Kết luận

Điểm mới rút ra từ cả sáu mảng: chỗ cần đầu tư nhất lại là chỗ rẻ nhất. Kịch bản viết bằng "nhưng/vì thế", 30 giây đầu được viết và thử nhiều bản, và một giọng cố định gần như không tốn credit. Thế nhưng dữ liệu của YouTube, của Galloway và của MrBeast đều chỉ về đúng những thứ này. Chỗ đắt nhất là người dẫn diễn bằng video AI. Phần này chỉ nên dùng ở nơi diễn xuất thật sự mang cảm xúc: khoảnh khắc người dẫn khựng lại, cúi đầu, nhìn sang hình lịch sử. Hooks gọi đó là phản ứng, và đó là thứ code không làm nổi. Mọi thứ còn lại (bản đồ, số liệu, chữ, nhịp nhạc) nên chuyển sang nhánh code, nơi sửa một dòng là xong.

Bài học thứ hai là tiết chế, và nó hiện ra ở mọi tầng: nhạc rút đi khi thông tin nặng nhất được nói, màu chỉ giảm bão hòa khi truyện cần, người dẫn đứng yên lâu hơn ở đoạn tang thương, và không chiếu khoảnh khắc chết. Điều này vừa đúng đạo đức tài liệu (APA, Muzzey) vừa đúng luật quảng cáo của YouTube. Với một kênh dùng AI, đây cũng là cách chứng minh mình không phải "inauthentic content": mỗi tập có góc nhìn, nguồn và chủ ý riêng. Điều chưa biết lớn nhất là người dẫn hiện hình có giữ chân tốt hơn kiểu chỉ có giọng hay không, vì chưa kênh lớn nào làm và công bố số liệu. Hãy đo câu trả lời đó trên chính kênh của bạn, qua chỉ số Intro của 10 tập đầu.
