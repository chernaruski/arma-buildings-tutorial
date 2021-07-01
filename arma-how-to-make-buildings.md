# Introduction

The following tutorial isn't a candidate for the best practice of creating Arma assets or any other aspect of modeling/texturing/etc. It was written as-is from a personal amateur experience. I'm just passing the knowledge I've gathered, creating Arma building assets without being a professional 3d artist in my free time. Some things in this tutorial might not be optimal or correct. Therefore I insist that you still dive into official documentation and other information sources and check for additional info.

In addition, the following tutorial is not covering the basics of 3D modeling, and it assumes readers have some degree of understanding and idea of its process. 
Also, it's not covering the use of different software such as Photoshop, Substance Painter, Marmoset Toolbag, and others. It only mentions few actions involved.

The main focus of this tutorial is a production pipeline for Arma 3 buildings modeling and the different nuances involved.


# Tools

I work with the following tools:

- 3ds Max / or any other 3D editor (Tho I work with 3dmax, and you will have to figure out equal features used in your editor)
- Adobe Photoshop
- Substance Painter
- Marmoset Toolbag
- ShaderMap
- PureRef
- Arma Tools
- Mikero Tools
- Notepad++ / Any other proper text editor

# References

The first thing to do is to gather as many references as possible. References that will be your inspiration, guide, and reminder of how things look and feel in real life.
I recommend using PureRef (www.pureref.com) for dumping & working with the references you find.

## Blueprints
When modeling buildings, the most valuable reference is the blueprints (floor plans). They can often be found for free all over the internet. 
My personal recommendation - https://vk.com/tiparh , a VK group where people have gathered A LOT of images and plans of the typical Soviet architecture. 

![Name](/assets/img/refs_1.png "tooltip text")
![Name](https://i.imgur.com/hjyTxy1.png "tooltip text")


## Photos
Search the web or make as many reference photos of your own and use it. Not necessarily the exact building you are modeling. Something similar should do too. You will need photos of the interior, exterior, roof, fundament, stairs. Basically, everything you can think of.

## Official Documentation
Sometimes you can even find full design documentation for a building. These contain descriptions of materials used, dimensions, etc.

![Name](/assets/img/refs_4.png "tooltip text")

## 3D models
You might find already modeled buildings at 3D model resources/marketplaces.You might even be able to afford/buy them. 
But do not delude yourself. It usually takes more time to redo and prepare the source model for Arma import, if possible at all. As references tho, they are pretty good and will be an additional "interactive blueprint."

![Name](/assets/img/refs_3.png "tooltip text")

## Other games
It's possible, someone already modeled and used something similar or exactly the same model in the game. He probably had the same issues as you will - poly count, optimization, textures, etc. Use it. Check how other people tackled these problems. Get inspired by the look or overall setting.

![Name](/assets/img/refs_2.png "tooltip text")

## Video
You won't believe it, but there are people who upload video reviews of elevators, house entrances, or buildings. This also can help us create a nice looking model.

# Size and Playability
You must remember, you are creating a game model and not real life. Therefore, sometimes you will have to make a wise decision about the real dimensions and the one you will need in the game.

For example, sometimes, the blueprint says the door frame should be only 80 cm.  In-game, there is no way player character can pass through that. Do not follow the blueprint blindly. Adjust it accordingly if you see that the real dimensions are not playable.

From my experience, I found out that these standard dimensions and limitations are the best:

Doors: Width 100-120cm. Height 200-220cm.
Corridors or staircase: Width 150cm. minimum.
Ceilings: Height 270-300cm.

I've created a simple dimensioning "test" that helps estimate the correct dimensions.

# Prototype
First, we need to make sure everything we planned works in-game properly. We create a quick prototype with basic geometry, no textures. This will make our lives much easier. Otherwise, if you happen and find mistakes at the advanced modeling stages (after the baking of light, masks, etc.), it will cost you a lot of effort and time to fix it.

For example, let us focus on the 80cm—door frame I've mentioned earlier. If you find out that the game character can't go through it at the very end, you will have to adjust the geometry, redo the textures accordingly, bake the light again, etc. It's wise to have a rough prototype, even from basic blocks/boxes, to see how it feels and plays, how the character moves inside the building, how he can take positions by the windows, etc. These first steps are essential and sometimes even can change the initial idea.

It's better to test some idea and/or functionality first than realize only in the end that it doesn't work. For example, this is how I've tested if a player can get out of the window, walk the pipe and climb up to the roof using the ladder:

[![](https://res.cloudinary.com/marcomontalbano/image/upload/v1624684875/video_to_markdown/images/youtube--UZkex4OHzUg-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=UZkex4OHzUg "")

  
# Planning
For full-fledged planning, we need to go over and fully comprehend the previous steps. At this stage, you need to plan how many parts your building will have, how many textures, prepare the textures folder and different textures, etc. Write step after step what you about to do.

# Textures
For good-looking materials, we need good textures. Properly looking material should have a base color map, normal map, roughness map (in Arma 3, roughness map needs to be converted into SMDI texture).

There are three main ways to get the textures for your project :

## Buying PBR textures
This is the easiest way. Almost any texture you might be interested in can be found on various sites for a fee (some for free). Usually, they are already of good quality.
Here is my resource list:
- [Textures.com](https://www.textures.com/)
- [Adobe Substance 3D Assets](https://substance3d.adobe.com/assets/)
- [Quixel Megascans](https://quixel.com/megascans/home/)
- [GameTextures,com](https://gametextures.com/)
- [CGTrader](https://www.cgtrader.com/3d-models/textures)
- [3ddd](https://3ddd.ru/3dmodels?cat=teksturi&subcat=teksturi_kirpich&page=1)

## Generating PBR Textures 
You can often use this method to speed things up or use it for minor detailed textures. The idea is to use a base color texture, usually made of high quality photos, and generate the rest of texture maps via software such as ShaderMap or Substance B2M.

| ![Image from ShaderMap site](/assets/img/tex_1.png "ShaderMap") | 
|:--:| 
| *Image from ShaderMap site* |


| ![Image from substance3d.adobe.com site](/assets/img/tex_2.png "substance3d.adobe.com") | 
|:--:| 
| *Image from substance3d.adobe.com site* |


This an example of my "handmade" texture:
| ![My texture](/assets/img/tex_3.png "My texture") | 
|:--:| 
| *My texture* |


| ![My Material Preview](/assets/img/tex_4.png "My Material Preview") | 
|:--:| 
| *My Material Preview* |


## Creating PBR Textures
If you couldn't find any required textures using the above method, you can create them in Substance Painter.

For example, this is how I made a texture for the building tiles:
| [![Building tiles texture](https://res.cloudinary.com/marcomontalbano/image/upload/v1624625868/video_to_markdown/images/youtube--A3mcL3jteS0-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=A3mcL3jteS0 "Building tiles texture") | 
|:--:| 
| *Building tiles texture* |


And in this one I tried to paint a damaged window glass:
| ![Damaged window glass texture](/assets/img/tex_5.png "Damaged window glass texture") | 
|:--:| 
| *Damaged window glass texture* |


## Using standard textures
In the end, you can always use the standard textures we already have in-game.

# Modeling
## The impact of multimaterial on the building modeling process.
Multimaterial is the type of material the game engine applies according to how we colored the building. WIKI: https://community.bistudio.com/wiki/Multimaterial
If you did not understand anything from the official documentation, don't sweat about it, nor do I.

The amount of materials used plays a significant role in the model's performance and the game's FPS. Simply put, this is the number of different textures we will be using. Multimaterial allows 4 textures to be used as 1 material, thus making significant optimization improvements. Our goal is to minimize the number of materials used.
So it is important, right from the beginning, to take this into account.

For the main building model, we must use multimaterial. For details, we need to compile a texture atlas. Thriving to paint our model with the minimal number of textures.


First, I will demonstrate how it works.

When using multimaterial, you need to create a second UV channel on the model:
| ![second UV channel](/assets/img/multimat_7.png "second UV channel") | 
|:--:| 
| *second UV channel* |

| ![Mask](/assets/img/multimat_3.png "Mask") | 
|:--:| 
| *Mask* |

| ![Mask](/assets/img/multimat_1.png "Mask") | 
|:--:| 
| *Mask for the model* |

| ![Mask](/assets/img/multimat_2.png "Mask") | 
|:--:| 
| *Results* |

Let's add a macro texture (ignore the artistic side of things, this is just a demo):

| ![Macro texture](/assets/img/multimat_4.png "Macro texture") | 
|:--:| 
| *Macro texture* |

| ![Macro texture](/assets/img/multimat_5.png "Macro texture") | 
|:--:| 
| *Results with macro texture* |

| ![Macro texture](/assets/img/multimat_6.png "Macro texture") | 
|:--:| 
| *Results with macro texture* |

ADSHQ adds baked light, which gives the model a more realistic look
| ![ADSHQ Texture](/assets/img/multimat_8.png "ADSHQ Texture") | 
|:--:| 
| *ADSHQ Texture (model lighting)* |

| ![In game](/assets/img/multimat_9.png "In game") | 
|:--:| 
| *In game* |

О влиянии освещения будет рассказано далее.

Сам мультиматериал (файл .rvmat), использованный в примере:
```cpp
ambient[]={0.7,0.7,0.7,1};
diffuse[]={0.4,0.4,0.4,1};
forcedDiffuse[] = {0.0,0.0,0.0,0.0};
emmisive[] = {0.0,0.0,0.0,1.0};
specular[] = {0.05,0.05,0.05,1.0};
specularPower = 0;
PixelShaderID = "Multi";
VertexShaderID = "Multi";

class TexGen0 { uvSource = "tex"; class uvTransform  { side[] = {1,0,0}; up[] = {0,1,0}; dir[] = {0,0,1}; pos[] = {0,0,0};};};
class TexGen1 { uvSource = "tex"; class uvTransform  { side[] = {1,0,0}; up[] = {0,1,0}; dir[] = {0,0,1}; pos[] = {0,0,0};};};
class TexGen2 { uvSource = "tex"; class uvTransform  { side[] = {1,0,0}; up[] = {0,1,0}; dir[] = {0,0,1}; pos[] = {0,0,0};};};
class TexGen3 { uvSource = "tex"; class uvTransform  { side[] = {1,0,0}; up[] = {0,1,0}; dir[] = {0,0,1}; pos[] = {0,0,0};};};
class TexGen4 { uvSource = "tex1"; class uvTransform  { side[] = {1,0,0}; up[] = {0,1,0}; dir[] = {0,0,1}; pos[] = {0,0,0};};};
class TexGen5 {	uvSource = "tex"; class uvTransform	{ aside[] = {1,0,0}; up[] = {0,1,0}; dir[] = {0,0,1}; pos[] = {0,0,0};};};
class TexGen6 { uvSource = "tex"; class uvTransform	{ aside[] = {1,0,0}; up[] = {0,1,0}; dir[] = {0,0,1}; pos[] = {0,0,0};};};
class TexGen7 {	uvSource = "tex"; class uvTransform	{ aside[] = {1,0,0}; up[] = {0,1,0}; dir[] = {0,0,1}; pos[] = {0,0,0};};};

//BLACK
class Stage0 { texture="buildings_tutorial\data\plaster_co.paa"; texGen = 0; };
class Stage5 { texture="#(argb,8,8,3)color(1,0,1,0,SMDI)"; texGen = 5; };
class Stage11 {	texture="buildings_tutorial\data\plaster_nohq.paa"; texGen = 0; };

//RED
class Stage1 { texture="buildings_tutorial\data\brick_co.paa"; texGen = 1; };
class Stage6 { texture="#(argb,8,8,3)color(1,0,0,0,SMDI)"; texGen = 6; };
class Stage12 {	texture="buildings_tutorial\data\brick_nohq.paa"; texGen = 1; };

//GREEN
class Stage2 { texture="buildings_tutorial\data\wall_paint_co.paa"; texGen = 2; };
class Stage7 { texture="#(argb,8,8,3)color(1,0,0,0,SMDI)"; texGen = 7; };
class Stage13 {	texture="buildings_tutorial\data\wall_paint_nohq.paa"; texGen = 2; };

//BLUE
class Stage3 { texture="buildings_tutorial\data\tiles_co.paa"; texGen = 3; };
class Stage8 { texture="#(argb,8,8,3)color(1,0,1,0,SMDI)"; texGen = 3; };
class Stage14 { texture="buildings_tutorial\data\tiles_nohq.paa"; texGen = 3;};

//Masks
class Stage4 { texture="buildings_tutorial\multimat_demo\data\mask.paa"; texGen = 4; };
class Stage9 { texture="buildings_tutorial\multimat_demo\data\texture_mc.paa"; texGen = 4; };
class Stage10 { texture="buildings_tutorial\multimat_demo\data\light_gi_adshq.paa"; texGen = 4; };
```

## Базовые техники и принципы
- Учесть удобство при экспорте/импорте - разделять модель на селекшены!
- Декали
- Моделируем сначала уникальные части, дубликаты заливаем красным для корректной запечки
- Заранее продумываем части модели для мультиматериала
- Если площадь большая - то в мультиматериале может быть меньше 4 текстур
- Иметь ввиду уменьшение количества материалов в лодах разрешения
- Собираем всё после запечки и маски
- Нужно иметь ввиду модель под землей, метра полтора
- Оптимизация модель 1 текстурой на ближних лодах не пройдёт
- Разные цвета маски не должны соприкасаться! UV-шелы отдельных ид - отдельно!

## Разделение модели на части

Представим, что у нас есть вот такая модель здания:
![Name](/assets/img/model_1.png "tooltip text")

Очевидно, что данная модель может использовать довольно много текстур. Навскидку:
- Внешние стены
- Фундамент
- Крыша
- Полы в комнатах
- Стены в комнатах
- Потолки в комнатах
- Полы в подъезде
- Стены в подъезде
- Потолок в подъезде
- Лестничные пролёты

Я бы предложил разделить эту модель на условные 3 части:
- Внешние стены
- Комнаты
- Подъезд

![Name](/assets/img/model_2.png "tooltip text")

Заметьте, как сделаны оконные проёмы - окна обычно вставлены примерно посередине, так, что с внешней стороны проём "уличный" - штукатурка, кирпичи и т.п., а с "внутренней" стороны - побелка, краска и т.п.

![Name](/assets/img/model_3.png "tooltip text")

Итого, вот такое получилось разделение:

![Name](/assets/img/model_4.png "tooltip text")

Каждую такую часть мы покрасим мультиматериалом, сократив таким образом количество материалов до 3 (вместо 10 из списка выше). Для этого нам первым делом нужно сделать развертку на втором UV-канале. Каждую часть здания я будут далее называть:
- Mat_1 (внешние стены)
- Mat_2 (комнаты)
- Mat_3 (подъезд)

Обычно я использую автоматическую развертку и почти никогда не правлю её руками.

Развертка для Mat_1:

![Name](/assets/img/model_5.png "tooltip text")

Развертка для Mat_2:

![Name](/assets/img/model_6.png "tooltip text")

Развертка для Mat_3:

![Name](/assets/img/model_7.png "tooltip text")

Развертки для Mat_1 и Mat_3 получились в принципе неплохими с точки зрения размера текселя. А вот с Mat_2 есть небольшие проблемы - размеры полигонов довольно маленькие (на самом деле терпимо, в целях обучения будет считать, что маленькие).

Давайте внимательнее посмотрим на Mat_2:

![Name](/assets/img/model_8.png "tooltip text")

Видно, что комнаты в правом и левом крыле здания одинаковые, но отзеркаленные. В каждом крыле комнаты на 1 и 2 этажах одинаковые. В принципе, маска и освещение у них должно быть одинаковое. В целях оптимизации мы можем пока убрать одинаковые (отзеркаленные - тоже будем считать одинаковыми) части. Мы сделаем маску и освещение только для уникальных частей здания, а потом их раскопируем и отзеркалим опять. Я буду заливать красным цветом те части здания, которые не будут участвовать в маске и запечке освещения.

![Name](/assets/img/model_9.png "tooltip text")

Заметьте - оконные проёмы я тоже залил красным.

Таким же образом поступим и с Mat_1:

![Name](/assets/img/model_10.png "tooltip text")

Здесь мы вырезали немного, только оконные проёмы.

В Mat_3 вообще вырезать нечего:

![Name](/assets/img/model_11.png "tooltip text")

Если бы это был девитиэтажный дом, то скорее всего Mat_3 также бы подвергся вырезанию одинаковых частей, но в таком небольшом здании можно оставить всё как есть.

Итого, мы вырезали довольно большой кусок здания:

![Name](/assets/img/model_12.png "tooltip text")

Теперь нужно ещё раз сделать UV на 2 канале:

Mat_1 (я немного повращал UV-шелы, чтобы куски здания стояли вертикально - при случае будет удобнее в фотошопе что-то дорисовывать. Мелочь, а приятно)

![Name](/assets/img/model_13.png "tooltip text")

Mat_2 стал значительно крупнее:

![Name](/assets/img/model_14.png "tooltip text")

Mat_3 не изменился

![Name](/assets/img/model_15.png "tooltip text")

Теперь каждый материал можно разбить на отдельные текстуры (максимум 4 текстуры в материле)

Mat_1:
- Red: Внешние стены
- Green: Фундамент
- Blue: Крыша
- Black: Остаётся в запасе, можно будет далее смешать с внешними стенами

![Name](/assets/img/model_20.png "tooltip text")

Mat_2:
- Red: Стены
- Green: Потолок
- Blue: Пол
- Black: Остаётся в запасе, можно будет далее смешать со стенами

![Name](/assets/img/model_21.png "tooltip text")

Mat_3:
- Red: Стены
- Green: Пол
- Blue: Бетон
- Black: Потолок

![Name](/assets/img/model_22.png "tooltip text")

В итоге, получили такое разделение:

![Name](/assets/img/model_26.png "tooltip text")

Теперь можно запечь Diffuse каждого материала (селекшена) и получить маску.

![Name](/assets/img/model_52.png "tooltip text")

![Name](/assets/img/model_53.png "tooltip text")

![Name](/assets/img/model_54.png "tooltip text")

Далее, нужно запечь освещение. Раньше я использовал для этого Substance Painter и запекал там Ambient Occlusion, но сейчас предпочитаю запекать глобальное освещение, например, в 3ds Max. Основное преимущество Ambient Occlusion, что это очень быстро. За считанные минуты можно получить хороший результат. Запекание же глобального освещения медленнее в разы. Для этого руководства я запекал свет на очень низком качестве около часа.

Процесс запекания освещения на низком качестве - видна сильная зернистость.
![Name](/assets/img/model_16.png "tooltip text")

![Name](/assets/img/model_17.png "tooltip text")

Результат:

![Name](/assets/img/model_18.png "tooltip text")

![Name](/assets/img/model_19.png "tooltip text")

К счастью, можно немного схитрить. Воспользоваться blur в Photoshop:

![Name](/assets/img/model_23.png "tooltip text")

![Name](/assets/img/model_25.png "tooltip text")

После этого финта качество освещения на довольно приличном уровне.

Для внешних стен я запёк Ambient Occlusion (потому, что запекая глобальное освещение я получил лишь сплошной белый цвет):

![Name](/assets/img/model_27.png "tooltip text")

Можно полюбоваться на результат в Marmoset:

![Name](/assets/img/model_28.png "tooltip text")

![Name](/assets/img/model_29.png "tooltip text")

![Name](/assets/img/model_30.png "tooltip text")

![Name](/assets/img/model_31.png "tooltip text")

Итого, мы сделали маску и освещение:

![Name](/assets/img/model_32.png "tooltip text")

Если назвать файлы со светом как name_adshq, то Image2Paa сконвертирует их в правильную текстуру:

![Name](/assets/img/model_55.png "tooltip text")

Либо, name_as:

![Name](/assets/img/model_56.png "tooltip text")

Обычно я использую _as для внешних стен, а _adshq для внутренних помещений.

Теперь можно натянуть текстуры на модель. В 3ds Max я использую материал типа SubObject для этого. Каждому face в объекте можно назначить свой идентификатор, соответствующий определенной текстуре.

![Name](/assets/img/model_34.png "tooltip text")

![Name](/assets/img/model_33.png "tooltip text")

Теперь можно удалить то, что я залил красным цветом и раскопировать части объекта из покрашенной части:

![Name](/assets/img/model_35.png "tooltip text")

Таким образом, мы достигли эффекта "оверлаппинга" - развертка скопированных частей лежит "друг на друге", и имеет одинаковую маску и освещение.

Далее, нужно сделать геометрию - я это делаю обычным блоками.

![Name](/assets/img/model_36.png "tooltip text")

Далее - Roadway - это то, где будет ходить персонаж

![Name](/assets/img/model_37.png "tooltip text")

Теперь, наконец, можно импортнуть всё в игру и посмотреть:

![Name](/assets/img/model_45.jpg "tooltip text")

![Name](/assets/img/model_39.jpg "tooltip text")

![Name](/assets/img/model_40.jpg "tooltip text")

![Name](/assets/img/model_41.jpg "tooltip text")

![Name](/assets/img/model_42.jpg "tooltip text")

![Name](/assets/img/model_43.jpg "tooltip text")

Обратите внимание - я намерено допустил ошибку, не отделив на маске разные цвета друг от друга. И поэтому место их соприкосновения выглядит вот так:

![Name](/assets/img/model_44.jpg "tooltip text")

Нет чёткой границы между разными текстурами. Здесь это выглядит приемлимо, но в большинствен случаев нужно позаботиться о том, чтобы UV-шелы с разными цветами не соприкасались друг с другом.

Можно поиграть с маской и макротекстурой:

![Name](/assets/img/model_46.jpg "tooltip text")

![Name](/assets/img/model_47.jpg "tooltip text")

Получилось ужасно, но суть вы должны понять. Обратите внимание - я хотел создать эффект отлетевшей штукатурки с помощью маски, но очевидно, что это выглядит очень плохо. Такие вещи нужно делать с помощью декалей.

![Name](/assets/img/model_48.jpg "tooltip text")

![Name](/assets/img/model_49.jpg "tooltip text")

Кстати, зацените как плохо смотрится та же модель без запеченного освещения:

![Name](/assets/img/model_50.jpg "tooltip text")

![Name](/assets/img/model_51.jpg "tooltip text")

## Развертка UV2
- Плотность
- Паддинг
- Оверлаппинг
# LOD Geometry
- Моделируем блоками
- Назначаем вес
# LOD FireGeometry
- Разделить на селекшены по типу материала на этапе моделирования, чтобы при экспорте удобно назначать пенетрацию
# LOD Shadow
- Дополнительные детали, чем в просто геометрии
# LOD ViewGeometry
# LOD Roadway
- Наименовать селекшены по типу покрытия
- Назначить текстуру на разные покрытия
# LOD Path
- Позиции
- Действия
- Входные точки
# LOD Memory
- Что и для чего
# LOD HitPoints
- Что и для чего
# Материалы
- Супершейдер
- Мультиматериал
- Примеры
# Освещение
- Конвертация в AS или ADSHQ
- При запечке света нужны все другие детали, которые не запекаем, кроме окон и дверей

## Советы бывалого
Может показаться хорошей идеей какой-нибудь средний лод оптимизировать путём радикального сокращения текстур, сделав атлас, например вот так:
![Name](/assets/img/hints_2.png "tooltip text")
![Name](/assets/img/hints_1.png "tooltip text")

Модель вроде и смотрится неплохо (особенно с дальней дистанции), но т.к. материалы будут разные, то переходы между ними будут (когда игра будет менять лоды) - будут очень заметными.

# Global illumination или Ambient Occlusion?
| ![GI](/assets/img/gi_vs_ao_1.png "GI") | 
|:--:| 
| *Global ullumination* |

| ![AO](/assets/img/gi_vs_ao_2.png "AO") | 
|:--:| 
| *Ambient occlusion* |

| ![GI](/assets/img/gi_vs_ao_3.png "GI") | 
|:--:| 
| *Global ullumination* |

| ![AO](/assets/img/gi_vs_ao_4.png "AO") | 
|:--:| 
| *Ambient occlusion* |

| ![GI](/assets/img/gi_vs_ao_5.png "GI") | 
|:--:| 
| *Global ullumination* |

| ![AO](/assets/img/gi_vs_ao_6.png "AO") | 
|:--:| 
| *Ambient occlusion* |

# Макротекстура
- Рисуем в фотошопе \ Субстанс паинтере
# Resolution Lods
- Принципы создания лодов - в 2 раза меньше полигонов чем в предыдущем, также уменьшать количество материлов
# Окна
- Моделирование, текстуры
- Моделирование хитпоинтов, эффектов и меморипоинтс
- Геометрия и ФайрГеометрия
- Тула для именования селекшенов
- Повреждения
# Двери
- Моделирование, текстуры
- Моделирование меморипоинтс
- Геометрия и ФайрГеометрия и ВьюГеометрия
- Тула для именования селекшенов
# Proxy
- Добавления прокси
- Прокси окклюдер
# Повреждения
- Повреждения материалов
- Повреждения моделей

# Экспорт модели
- Можно наименовать селекшены для автоматического разброса по лодам
- Почистить модель после
- Добавить намед пропертис
- Замена текстур на материалы
# Конфиг
- Базовый конфиг
- Шаблоны для кода
- Отдельно по частям
# Упаковка и запуск
- Mikero Tools
- Добавление мода
