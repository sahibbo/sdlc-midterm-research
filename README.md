# SDLC prosesində problemlərin səbəbləri və həll yolları

**Sahib Aslanov**  
Proqram təminatının inkişafı və dizaynı üzrə kollekvium araşdırması  
29 oktyabr 2026

## Araşdırmanın məqsədi

Bir proqramın gecikməsi barədə eşidəndə ilk ağla gələn səbəb adətən kodun vaxtında yazılmamasıdır. Mən bu mövzuda başqa bir suala cavab axtardım: komanda işi vaxtında görsə də, layihə niyə uğursuz nəticələnə bilər? Araşdırmanı bu sual üzərində qurdum. Çünki yanlış başa düşülmüş bir tapşırığın vaxtında yerinə yetirilməsi də istifadəçiyə lazım olan nəticəni verməyəcək.

Mövzuya baxışım budur ki, SDLC-də əsas çətinlik mərhələlərin adlarını bilməkdən çox, bir mərhələdə qəbul edilən qərarın sonrakı işə təsirini anlamaqdır. Əvvəldə cavabsız qalan sual sonradan dizayn dəyişikliyi, yenidən yazılan kod və təkrar test kimi qarşımıza çıxa bilər. Belə vəziyyətdə gecikmə problemin görünən hissəsi olur.

Müəllimin verdiyi ardıcıllığa uyğun olaraq iki Medium məqaləsi, bir LinkedIn məqaləsi və fərqli mənbə kimi AWS-in izahını seçdim. Əvvəlcə hər birinin əsas fikrini və ondan çıxardığım nəticəni qeyd edirəm. Sonra yanaşmaları müqayisə edib universitet üçün fənn qeydiyyatı sistemi nümunəsində tətbiq edirəm. Bu nümunə və onun hesablamaları mövzunu izah etmək üçün qurulub; real layihəyə aid nəticələr kimi təqdim olunmur.

## 1 Medium üzrə birinci məqalə

**Məqalə:** Understanding SDLC: Requirement Gathering and Analysis  
**Müəllif:** Anjalee Amarakoon  
**Tarix:** 17 avqust 2025  
**Link:** [Məqaləni Medium platformasında aç](https://medium.com/@amarakoonanjalee11/requirement-gathering-and-analysis-the-first-step-to-great-software-bd1d69e071b9)

Müəllif proqramın nə etməli olduğunu müəyyənləşdirmək üçün istifadəçi və sifarişçi ilə danışmağın vacibliyini izah edir. Natamam tələblər lazımsız funksiyalara, vaxt itkisinə və gözləntilərə uyğun gəlməyən məhsula səbəb ola bilər. Təklif olunan yollar tələbləri yazmaq, ziddiyyətləri aradan qaldırmaq, imkanlara uyğunluğunu yoxlamaq və sadə prototiplərlə dəqiqləşdirməkdir. [1]

**Çıxardığım nəticə.** Tələblərin toplanmasını sadəcə müştərinin istəklərini siyahıya almaq kimi başa düşməmək lazımdır. Komanda həmin istəklərin nə demək olduğunu da razılaşdırmalıdır. Mənim üçün bu məqalənin əsas faydası işə başlamazdan əvvəl hansı sualları verməli olduğumuzu göstərməsidir.

Məqalənin dili sadədir və mövzuya giriş üçün əlverişlidir. Ancaq konkret layihələr üzrə müqayisəli ölçmələr təqdim etmir. Buna görə onun tövsiyələrini izah kimi qəbul edirəm; hər layihədə eyni nəticənin alınacağını göstərən sübut kimi yox.

## 2 Medium üzrə ikinci məqalə

**Məqalə:** Common SDLC and Testing Mistakes That Cost Startups Time and Money  
**Müəllif:** Ubertesters  
**Tarix:** 4 dekabr 2025  
**Link:** [Məqaləni Medium platformasında aç](https://ubertesters.medium.com/common-sdlc-and-testing-mistakes-that-cost-startups-time-and-money-1e03f55b7722)

Məqalə tələsik inkişaf prosesində planlaşdırmanın və keyfiyyət yoxlamalarının zəifləməsini müzakirə edir. Testlərin sona saxlanılması, müxtəlif cihazların və real istifadə şəraitinin nəzərə alınmaması vurğulanır. Müəllif erkən yoxlamaları, avtomatlaşdırılmış testlərlə insan tərəfindən aparılan yoxlamaların birlikdə istifadəsini və istifadəyə verildikdən sonra rəylərin izlənməsini təklif edir. [2]

**Çıxardığım nəticə.** Bir funksiyanın normal şəraitdə işləməsi onun bütün vacib hallarda düzgün davranacağını göstərmir. Yoxlamanın məqsədini əvvəlcədən müəyyənləşdirmək lazımdır: hansı səhvi tapmağa çalışırıq və həmin səhv istifadəçiyə nə qədər təsir edəcək?

Mənbə test xidməti göstərən şirkətə məxsusdur və məqalədə bu xidmət də təbliğ olunur. Ümumi test tövsiyələri faydalıdır, amma konkret xidmətin hər komanda üçün ən yaxşı həll olduğu nəticəsini çıxarmıram. Başlanğıcdakı startapların uğursuzluğu barədə geniş faiz iddiasını da SDLC səhvlərinin payını sübut edən məlumat kimi istifadə etmirəm.

## 3 LinkedIn məqaləsi

**Məqalə:** Why application development projects fail  
**Müəllif:** Pankaj Phukane  
**Tarix:** 11 mart 2026  
**Link:** [Məqaləni LinkedIn platformasında aç](https://www.linkedin.com/pulse/why-application-development-projects-fail-pankaj-phukane-csm--ro0oc)

Müəllif öz peşə təcrübəsinə əsaslanaraq qeyri-müəyyən məqsədləri, razılaşdırılmamış prioritetləri, inteqrasiya çətinliklərini və məsuliyyət bölgüsündəki boşluqları araşdırır. Təklifləri uğur meyarlarını əvvəlcədən müəyyənləşdirmək, dəyişikliklərin təsirini qiymətləndirmək, məsul şəxsləri göstərmək və istifadəyə verildikdən sonrakı dəstəyi planlaşdırmaqdır. [3]

**Çıxardığım nəticə.** Proqramçıya verilən tapşırıqla sifarişçinin gözlədiyi nəticə arasında əlaqə qorunmalıdır. Əgər bir neçə tərəf fərqli şeylər istəyirsə, komanda hansına üstünlük verəcəyini bilməlidir. Əks halda görülən iş sonradan qəbul edilməyə bilər.

Bu məqalə ilk iki mənbəyə idarəçilik baxışı əlavə edir. Bununla belə, müəllifin uğursuzluqları əsasən idarəçiliklə əlaqələndirən fikrini bütün layihələr üçün ümumi qayda saymıram. Burada şəxsi təcrübə əsasında verilmiş şərh var; texnologiyanın yanlış seçilməsi və ya texniki həllin mümkünsüzlüyü də ayrıca araşdırılmalıdır.

## 4 Fərqli mənbədən seçilmiş məqalə

**Məqalə:** What is SDLC?  
**Mənbə:** Amazon Web Services  
**Link:** [Məqaləni AWS saytında aç](https://aws.amazon.com/what-is/sdlc/)

AWS planlaşdırma, dizayn, proqramlaşdırma, test, istifadəyə vermə və texniki xidmət fəaliyyətlərini ümumi proses daxilində izah edir. Müxtəlif inkişaf modellərinin fərqli məhdudiyyətlərini göstərir və təhlükəsizliyin proses boyunca nəzərə alınmasını vurğulayır. Testin proqramlaşdırma ilə paralel aparıla bilməsi də qeyd olunur. [4]

**Çıxardığım nəticə.** Mərhələləri sərt şəkildə bir dəfə keçilən pillələr kimi təsəvvür etmək düzgün olmaz. Yeni məlumat alındıqda əvvəlki qərara qayıtmaq lazım gələ bilər. Mənim üçün əsas məsələ bu qayıdışın səbəbinin və təsirinin aydın olmasıdır.

AWS-in izahı mövzunu bütöv görməyə kömək edir, amma konkret universitet layihəsinin neçə həftəyə bitəcəyini və hansı modeli seçməli olduğunu müəyyən etmir. Məqalənin sonunda öz məhsulları da təqdim olunur. Buna görə SDLC izahını həmin məhsullardan mütləq istifadə etmək tövsiyəsindən ayrı qiymətləndirirəm.

## 5 Dörd məqalənin müqayisəsi

| Mənbə | Problemi harada axtarır | Önə çıxardığı həll | Təkbaşına cavab vermədiyi sual |
|---|---|---|---|
| Medium 1 | Tələblərin anlaşılmasında | Ehtiyacları dəqiqləşdirmək | Dəyişikliklərə necə nəzarət edək |
| Medium 2 | Test və keyfiyyət işində | Erkən və real şəraitə uyğun yoxlama | Hansı funksiyanı əvvəl hazırlayaq |
| LinkedIn | Qərar və məsuliyyət bölgüsündə | Məqsəd və cavabdehliyi aydınlaşdırmaq | Texniki həlli necə quraq |
| AWS | Bütün inkişaf dövründə | Fəaliyyətləri əlaqələndirmək | Konkret layihəyə nə qədər resurs ayıraq |

Cədvəldəki son sütun mənim qiymətləndirməmdir. Məqalələrin müxtəlif suallara cavab verdiyini göstərmək üçün əlavə etmişəm. [1–4]

Müqayisədən çıxardığım fikir budur: tələblər barədə razılıq əldə etmək, sonra həmin razılığı proqramın davranışı ilə yoxlamaq lazımdır. Məqsəd yalnız yazılı sənədin olması deyil. Sənəddə razılaşdırılan qayda hazırlanmış sistemdə də görünməlidir. Testlərin çoxluğu da özü-özlüyündə kifayət etməz; yanlış qəbul edilmiş qaydanı yoxlayan testlər uğurlu keçə bilər.

Bu yanaşmalar arasında diqqət tələb edən bir məsələ var. Əvvəlcədən dəqiqlik istəmək bütün tələblərin birdəfəlik dəyişməz qalması demək deyil. Agile Manifesto prinsipləri dəyişən tələbləri qəbul etməyi, işləyən proqramı tez-tez təqdim etməyi və istifadəçi tərəfi ilə əməkdaşlığı vurğulayır. [5] Mənim nəticəm budur ki, komanda yeni ehtiyaclara açıq olmalı, eyni zamanda onların mövcud plana təsirini görünən etməlidir.

Bu dörd mənbə əsasında hansı səbəbin layihələrdə ən çox təkrarlandığını statistik olaraq müəyyən etmək olmaz. Mənbələr eyni üsulla aparılmış dörd tədqiqat deyil. Onlardan problemin müxtəlif tərəflərini görmək və tətbiq oluna biləcək suallar çıxarmaq üçün istifadə edirəm.

## 6 Universitet layihəsi üzərində tətbiq

### Nümunənin şərtləri

Təsəvvür edək ki, universitet tələbələrin seçmə fənlərə yazılması üçün kiçik bir sistem istəyir. Üç nəfərlik komandanın beş həftə vaxtı var. Əsas iş tələbənin açıq fənləri görməsi, uyğun fənnə yazılması və öz qeydiyyatını yoxlamasıdır. Universitet tərəfdən bir əməkdaş isə fənlərin yer sayını və qeydiyyat tarixlərini idarə edir.

Bu nümunədə əlavə funksiyalar kimi avtomatik gözləmə siyahısı və e-poçt bildirişləri də istənilə bilər. Lakin onların ilk versiyaya daxil ediləcəyi əvvəlcədən qəbul olunmur. Aşağıdakı qərarlar bu şərtlər üçün təklif etdiyim yanaşmadır.

### Cavabsız qalan qeydiyyat qaydaları

Tutaq ki, komanda ilkin söhbətdə yalnız belə bir cümlə eşidir: tələbələr istədikləri fənnə asanlıqla yazılsınlar. Bu cümlə ekran hazırlamağa başlamaq üçün kifayət qədər aydın görünür. Ancaq qeydiyyat qaydasını müəyyənləşdirmir.

Məsələn, tələbə eyni fənnə iki dəfə yazıla bilərmi? Qeydiyyatı ləğv edəndə boş yer dərhal başqa tələbəyə açılmalıdırmı? Son tarix keçdikdən sonra universitet əməkdaşı dəyişiklik edə bilərmi? Bir boş yerə iki tələbə eyni anda müraciət etsə, sistem nə etməlidir?

Bu suallar cavabsız qalsa, proqramçı özü uyğun hesab etdiyi variantı seçəcək. Sonra sifarişçi başqa qayda gözlədiyini deyə bilər. Mən bu halda yalnız proqramçını səhv etməkdə günahlandırmazdım. Qərarın kimdən alınmalı olduğu və harada qeyd ediləcəyi əvvəlcədən müəyyənləşməyib.

İlk görüşdə tələbə ilə yanaşı qeydiyyatı idarə edən əməkdaşın da iştirakını təklif edərdim. Onlardan gündəlik istifadəni izah etmələrini istəyərdim. Sonra əsas ekranların sadə təsvirini göstərib bir qeydiyyat nümunəsini əvvəldən axıra qədər birlikdə keçərdim. Burada məqsəd gözəl dizayn seçməkdən əvvəl qaydaları görmək olardı.

### Tələbi yoxlanıla bilən qaydaya çevirmək

Bu sistem üçün aşağıdakı qəbul meyarlarını təklif edirəm. Bunlar konkret funksiyanın hansı şərtlə düzgün sayılacağını göstərir.

| Qayda | Yoxlama halı | Gözlənilən nəticə |
|---|---|---|
| Təkrar qeydiyyat olmamalıdır | Eyni tələbə eyni fənnə yenidən yazılır | İkinci qeyd yaradılmır |
| Yer sayı aşılmamalıdır | Bir boş yerə eyni anda iki müraciət gəlir | Yalnız biri qəbul edilir |
| Tarix məhdudiyyəti işləməlidir | Tələbə son tarixdən sonra müraciət edir | Qeydiyyat qəbul edilmir |
| Məlumat hər kəsə açıq olmamalıdır | Tələbə başqa tələbənin qeydini açmağa çalışır | Giriş rədd edilir |
| Xəta zamanı vəziyyət aydın qalmalıdır | Müraciətin cavabı gəlməzdən əvvəl bağlantı kəsilir | Yenidən yoxlama həqiqi vəziyyəti göstərir və təkrar qeyd yaratmır |

Mənim üçün bu cədvəlin faydası ondadır ki, sifarişçi ilə proqramçı eyni nəticəni müzakirə edə bilir. Son boş yerin iki nəfərə verilməsi barədə qərarı yalnız test mərhələsində öyrənsək, məlumatların saxlanması qaydasına da yenidən baxmaq lazım gələ bilər. Əvvəlcədən razılaşma isə dizayn zamanı bu halı nəzərə almağa imkan verir.

### Kiçik görünən əlavə funksiyanın təsiri

İkinci həftədə sifarişçi avtomatik gözləmə siyahısı istəyir. İlk baxışda bu, dolu fənnin yanında əlavə bir düymə kimi görünə bilər. Ancaq həmin düymənin arxasında yeni qaydalar var. Boş yer açıldıqda birinci tələbəyə nə qədər vaxt veriləcək? Cavab gəlməsə növbə kimə keçəcək? Tələbə artıq başqa fənnə yazılıbsa, əvvəlki sorğu qüvvədə qalacaqmı?

Mən bu dəyişikliyi avtomatik rədd etməzdim. Əvvəlcə onun ilk versiya üçün nə qədər vacib olduğunu soruşardım. Sonra komanda əlavə işi qiymətləndirərdi. Əgər beş həftəlik tarix dəyişmirsə, başqa funksiyanı sonrakı versiyaya keçirmək və ya gözləmə siyahısını daha sadə formada qurmaq müzakirə oluna bilər.

Qərarın qısa qeydini saxlamaq da faydalıdır: istək nədir, kim təsdiqləyib, təxmini nə qədər iş yaradır və mövcud planda nə dəyişir? Belə olduqda bir neçə həftə sonra hamı fərqli razılaşma xatırlamaz.

Bu nümunədə dəyişiklik ehtiyacın daha yaxşı anlaşılmasından da yarana bilər. Buna görə hər yeni tələbi əvvəlki planın uğursuzluğu kimi qiymətləndirməzdim. Mənim üçün problem əlavə işin qəbul edilib, vaxtın və resursun dəyişmədiyi kimi davranılmasıdır.

### Ekranda görünməyən işin unudulması

Komanda fənn siyahısını tez hazırlaya bilər, çünki siyahıda göstəriləcək məlumatları özü yazır. Amma real sistemdə həmin məlumat başqa universitet sistemindən gəlməlidirsə, məsələ dəyişir. Tələbə və fənn kodlarının uyğunluğu, məlumatın yenilənməsi və əlaqə kəsiləndə davranış ayrıca yoxlanmalıdır.

Mən ilk həftədə kiçik bir məlumat mübadiləsi sınağı edərdim. Bir tələbə və bir fənn məlumatını qəbul edib düzgün oxuya bildiyimizi görmək kifayət edə bilər. Əgər məlumat mənbəyinə çıxış gecikirsə, bunu planda ayrıca asılılıq kimi göstərərdim. Gözləmə vaxtını komandanın işləməməsi ilə qarışdırmazdım.

Buradan çıxardığım fikir budur ki, layihədə çətinlik həmişə ən çox görünən ekranda olmur. Gözəl hazırlanmış interfeys məlumatın düzgün alındığını və qaydaların düzgün tətbiq edildiyini sübut etmir.

### Test və təhlükəsizlik üçün yer ayırmaq

Bu nümunədə əvvəlcə qeydiyyat qaydalarını ayrı-ayrılıqda, sonra onların birlikdə işləməsini yoxlamağı təklif edirəm. Məsələn, yer sayı qaydası tək müraciətdə işləyə bilər, eyni anda gələn müraciətlərdə isə pozula bilər. Digər bir yoxlamada qeydiyyatı ləğv etdikdən sonra boş yerin düzgün hesablandığına baxardım.

Təhlükəsizliyi də konkret istifadəçi hüquqları ilə əlaqələndirərdim. Tələbə yalnız öz qeydiyyatını dəyişməli, universitet əməkdaşının funksiyalarına çıxmamalıdır. Düyməni ekranda gizlətmək kifayət etməz; sistemin sorğunu qəbul edən hissəsi də istifadəçinin hüququnu yoxlamalıdır. Bunlar təklif etdiyim ssenarilərdir, bu sistemdə artıq tapılmış boşluqlar deyil.

NIST-in SSDF 1.1 sənədi təhlükəsiz proqram hazırlama təcrübələrinin müxtəlif SDLC modellərinə əlavə edilməsini tövsiyə edir. Məqsəd buraxılan proqramdakı zəiflikləri və onların təsirini azaltmaq, təkrarlanan problemlərin əsas səbəblərini aradan qaldırmaqdır. [6] Bu yanaşmaya uyğun olaraq istifadəçi hüquqlarını layihənin əvvəlində müəyyənləşdirib sonrakı yoxlamalara daxil edərdim.

Yoxlamaların hamısını avtomatlaşdırmağa da çalışmazdım. Təkrar qeydiyyat kimi sabit qaydaları avtomatik yoxlamaq münasibdir. Tələbənin ekranı başa düşməsi və xəta mesajından sonra nə edəcəyini bilməsi üçün isə insanın sistemi istifadə etməsi daha faydalı ola bilər.

### Vaxt və büdcənin sadə hesablanması

Bu hissədəki rəqəmlər şərtidir. Tutaq ki, üç nəfərin hər biri həftədə 10 saat ayıra bilir. Beş həftə üçün ümumi imkan 150 nəfər-saat edir: 3 nəfər × 10 saat × 5 həftə.

İlkin işləri 120 nəfər-saat qiymətləndirsək, 30 nəfər-saat ehtiyat qalır. Sonradan qəbul edilən əlavə funksiya 18, unudulmuş qaydanın düzəldilməsi isə 20 nəfər-saat tələb etsə, ümumi ehtiyac 158 nəfər-saata çatır. İlkin 120 saatlıq qiymətləndirmə ilə müqayisədə artım təxminən 31,7 faizdir. Mövcud imkanı isə 8 nəfər-saat keçir.

Bu hesabdan layihənin dəqiq neçə gün gecikəcəyini çıxarmaq olmaz. İşlərin hamısı paralel görülmür, bəziləri başqa işin bitməsini gözləyir. Amma hesab əlavə tapşırıqların mövcud imkanla uyğun gəlmədiyini göstərir.

Yalnız izah üçün bir nəfər-saatın qiymətini 10 AZN götürsək, ilkin əmək xərci 1200 AZN, dəyişmiş iş həcmi isə 1580 AZN edər. Bu, bazar qiyməti deyil və server, lisenziya kimi xərcləri əhatə etmir. Nümunənin məqsədi vaxt artımının büdcəyə necə keçə bildiyini göstərməkdir.

### Təhvil zamanı nəyə baxardım

Sistemin hazır sayılması üçün sadəcə bütün ekranların açılması ilə kifayətlənməzdim. Əsas qeydiyyat qaydalarının yoxlanması, vacib səhvlərin həlli və universitet əməkdaşının real iş ardıcıllığını yerinə yetirə bilməsi mənim üçün təhvil şərti olardı.

Məsələn, tələbə başqa şəxsin qeydiyyatını dəyişə bilirsə, bunu kosmetik səhv kimi sonraya saxlamazdım. Amma bir başlığın aralığı ideal deyilsə, əsas işə mane olub-olmadığına baxardım. Belə bölgü komandanın son günlərini daha vacib problemlərə ayırmağa kömək edər.

İlk istifadəyə verməni də bütün universitet üçün eyni anda etməzdim. Bu nümunədə bir qrupda sınaq istifadəsi təklif edərdim. Səhv görünəndə kimə müraciət olunacağı, dəyişikliklərin necə geri qaytarılacağı və qeydiyyat məlumatının necə qorunacağı əvvəlcədən müəyyənləşərdi. Beləliklə, təhvil qərarı ilə yanaşı sonrakı məsuliyyət də aydın qalardı.

## 7 Təklif etdiyim beş həftəlik iş planı

Bu bölgü nümunə sistem üçündür. Test hər həftənin işinə daxildir; dördüncü həftədə daha geniş birgə yoxlama aparılır.

| Həftə | Əsas iş | Həftənin sonunda görünən nəticə |
|---|---|---|
| 1 | Qaydaları razılaşdırmaq və məlumat mənbəyini sınaqdan keçirmək | Qəbul meyarları və sadə ekran təsviri |
| 2 | Fənlərin göstərilməsini və ilkin qeydiyyatı hazırlamaq | Göstərilə bilən kiçik işlək hissə |
| 3 | Yer sayı, tarix və istifadəçi hüquqlarını tamamlamaq | Əsas iş ardıcıllığının işləməsi |
| 4 | Eyni vaxtlı müraciətləri və xəta hallarını yoxlamaq | Vacib səhvlərin siyahısı və düzəlişlər |
| 5 | İstifadəçi yoxlaması, sınaq istifadəsi və təhvil | Razılaşdırılmış versiya və dəstək qeydi |

Hər həftənin sonunda komanda yalnız nə qədər kod yazdığını bildirməzdi. Hazırlanan hissəni göstərər, açıq qalan sualları qeyd edər və növbəti həftənin planını buna uyğun düzəldərdi. Bu cədvəl də dəyişməz vəd deyil; ilk həftədə imkanların fərqli olduğu görünsə, yenilənməlidir.

## 8 Yaxşılaşmanı necə qiymətləndirərdim

Təklif etdiyim prosesin faydasını da yoxlamaq lazımdır. Bu kiçik layihə üçün çoxsaylı göstəricilər seçməzdim. Hər həftə əvvəl hazır sayılıb yenidən açılan işləri, cavab gözləyən məsələləri və əlavə edilən funksiyaları qısa qeyd etmək kifayət edə bilər.

Yenidən açılan tapşırıqlarda səbəbi də ayırardım. Kod səhvi, sonradan dəyişən ehtiyac və əvvəlcədən danışılmamış qayda eyni hadisə deyil. Hamısını sadəcə səhv sayı kimi toplasaq, nəyi düzəltməli olduğumuzu görə bilmərik. Bu bölgü insanları günahlandırmaq üçün deyil, növbəti işi daha düzgün planlaşdırmaq üçündür.

Təhvildən sonra isə tələbənin əsas işi yerinə yetirib-yetirmədiyinə baxardım. Tələbə qeydiyyatın tamamlandığını başa düşmür və yenidən müraciət edirsə, ekranda texniki xəta olmasa da, istifadəçi üçün problem qalır. Deməli, uğuru təkcə bağlanmış tapşırıqların sayı ilə ölçmək mənim nümunəmdə yetərli deyil.

## 9 Yekun nəticəm

Mənim gəldiyim nəticə budur ki, SDLC düzgün qurulmayanda ən böyük itkilərdən biri artıq görülmüş işin yenidən görülməsidir. Bunun arxasında müxtəlif səbəblər dayana bilər. Universitet nümunəsində cavabsız qalmış qeydiyyat qaydası sonradan kodu və testləri dəyişdirməyə məcbur edir. Yeni funksiya isə ilk baxışda görünəndən çox iş yaradır. Bu təsirlər vaxtında nəzərə alınmayanda büdcə və təhvil tarixi əvvəlki kimi göstərilir, görüləcək iş isə artır.

Mən bu problemin həllini kiçik komanda üçün çoxlu sənəd yaratmaqda görmürəm. Əsas qərarların qısa və aydın qeydi, yoxlanıla bilən tələblər və hər həftə göstərilən işlək nəticə daha münasib başlanğıcdır. Məsələn, son boş yerə iki müraciətin necə cavablandırılacağını əvvəlcədən razılaşdırmaq bu layihə üçün uzun bir ümumi sənəddən daha faydalı qərar ola bilər.

Araşdırmadan sonra bütün gecikmələri zəif SDLC ilə izah etməyi də düzgün saymıram. Komandadan asılı olmayan səbəb, gözlənilməz texniki məhdudiyyət və ya sonradan yaranmış vacib ehtiyac ola bilər. Prosesin keyfiyyətini qiymətləndirəndə həmin vəziyyətin nə vaxt bilindiyinə, necə bildirildiyinə və planın buna uyğun dəyişdirilib-dəyişdirilmədiyinə baxardım.

Özüm belə bir layihəyə başlasaydım, əvvəlcə əsas istifadə qaydalarını dəqiqləşdirər, ən vacib işi görən kiçik versiya hazırlayar və onu istifadəçiyə göstərərdim. Sonra aldığım məlumata əsasən davam edərdim. Mənim üçün yaxşı qurulmuş SDLC-nin praktik dəyəri budur: komanda gördüyü işin hansı ehtiyacı qarşıladığını və yeni qərarın hansı işi dəyişdirdiyini izləyə bilir.

## 10 Mövzunu tamamlayan video materialları

### Simplilearn üzrə SDLC izahı

**Video:** What Is SDLC? Introduction to Software Development Life Cycle  
**Link:** [Videonu YouTube platformasında aç](https://www.youtube.com/watch?v=5b36UTNRmtI)

Videonun təsvirində SDLC-nin məqsədi, mərhələləri və modelləri göstərilir. Təsvirə əsasən mərhələlər 02:38, modellər isə 08:15 hissəsindən başlayır. Məqalələrdə işlənən anlayışları ümumi ardıcıllıqla nəzərdən keçirmək üçün əlavə materialdır. [7]

### Tom Wujec üzrə komanda işi nümunəsi

**Çıxış:** Build a tower, build a team  
**Link:** [Çıxışı TED saytında aç](https://www.ted.com/talks/tom_wujec_build_a_tower_build_a_team)

Çıxış spagetti, lent və marşmellou ilə qüllə qurmaq tapşırığı üzərindən komanda işini müzakirə edir. SDLC haqqında texniki dərs deyil. Mən onu komandaların birlikdə qərar verməsini düşünmək üçün əlavə nümunə kimi seçdim; proqram layihələrinin uğur faizini sübut etmək üçün istifadə etmirəm. [8]

### IBM üzrə inkişaf prosesinin izlənməsi

**Video:** IBM Process Mining & IBM BAMOE — SDLC Monitoring and Automation Demo  
**Link:** [Nümayişi YouTube platformasında aç](https://www.youtube.com/watch?v=Mx_ID8Uc_fk)  
**İzah:** [IBM-in nümayiş haqqında yazısı](https://community.ibm.com/community/user/blogs/aliannah-muzaffar/2026/04/28/ibm-process-mining-ibm-bamoe-sdlc-monitoring-and-a)

IBM-in təqdimatına görə nümayiş işlər arasındakı asılılıqların və ləngimə nöqtələrinin görünməsinə yönəlib. Mənim nümunəmdə bu, cavab və ya məlumat mənbəyini gözləyən işlərin ayrıca qeyd edilməsi ilə əlaqəlidir. Konkret IBM məhsullarının kiçik tələbə layihəsi üçün zəruri olduğu nəticəsini çıxarmıram. [9]

## İstinadlar

### Müqayisə olunan dörd əsas məqalə

1. Anjalee Amarakoon. *Understanding SDLC: Requirement Gathering and Analysis*. Medium, 17 avqust 2025. [Məqaləyə keçid](https://medium.com/@amarakoonanjalee11/requirement-gathering-and-analysis-the-first-step-to-great-software-bd1d69e071b9).
2. Ubertesters. *Common SDLC and Testing Mistakes That Cost Startups Time and Money*. Medium, 4 dekabr 2025. [Məqaləyə keçid](https://ubertesters.medium.com/common-sdlc-and-testing-mistakes-that-cost-startups-time-and-money-1e03f55b7722).
3. Pankaj Phukane. *Why application development projects fail*. LinkedIn, 11 mart 2026. [Məqaləyə keçid](https://www.linkedin.com/pulse/why-application-development-projects-fail-pankaj-phukane-csm--ro0oc).
4. Amazon Web Services. *What is SDLC?* [Məqaləyə keçid](https://aws.amazon.com/what-is/sdlc/).

### Əlavə yoxlama və video mənbələri

5. *Principles behind the Agile Manifesto*. [Prinsiplərə keçid](https://agilemanifesto.org/principles.html).
6. NIST. *SP 800-218, Secure Software Development Framework Version 1.1*. Fevral 2022. [Rəsmi nəşrə keçid](https://csrc.nist.gov/pubs/sp/800/218/final).
7. Simplilearn. *What Is SDLC? Introduction to Software Development Life Cycle*. YouTube, 17 avqust 2022. [Videoya keçid](https://www.youtube.com/watch?v=5b36UTNRmtI).
8. Tom Wujec. *Build a tower, build a team*. TED2010. [Çıxışa keçid](https://www.ted.com/talks/tom_wujec_build_a_tower_build_a_team).
9. Aliannah Muzaffar. *IBM Process Mining & IBM BAMOE — SDLC Monitoring and Automation Demo*. IBM Community, 28 aprel 2026. [İzaha keçid](https://community.ibm.com/community/user/blogs/aliannah-muzaffar/2026/04/28/ibm-process-mining-ibm-bamoe-sdlc-monitoring-and-a). [Videoya keçid](https://www.youtube.com/watch?v=Mx_ID8Uc_fk).

Mənbələrə baxış tarixi: 29 oktyabr 2026.
