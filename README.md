# interesting_docs
Свалка интересных неотсортированных документов
# Docs:
## 1. Диссертация на магистра на русском языке. Полезно для начинающих.
https://earchive.tpu.ru/bitstream/11683/40618/1/TPU410043.pdf
TPU410043

## 2. Большой проект украинцев в Португалии. Много полезного
https://vibromera.eu/
Balanset-1A Portable Balancer Manual - Dynamic Balancing.pdf
Составные части:
Digitaler Drehzahlmesser SEAFRONT HS2234 - на Амазоне 15,50€
ADXL335 board - Reichelt 13,00€, Alibaba - from 0,60€
Magnetständer, 60 kgf, mit Feineinstellung, INSIZE 6201-60 - https://www.insz.at/stander-und-messstative/magnetstander--60-kgf-mit-feineinstellung--insize--6201-60 22,00€
Цифровые весы от 10€

### Что можно улучшить
1. Убрать сигнальные провода от датчиков - через wifi, bluetooth. Вопрос с питанием - можно по проводу к powerbank. ChatGPT утверждает, что это возможно, если правильно обрабатывать, например, использовать приход пакета не как метку времени, а как номер оборота+период оборота.
2. Заменить датчик на ADXL355(2,4,8g) или 357(10,20,40g) - EVAL-ADXL355-PMDZ у Moser 49,00€, на Alibaba тоже. ChatGPT предлагает ADXL355+ESP32. Бюджетный вариант ADXL345 - 1,65€ https://www.amazon.de/ADXL345-3-Achsen-Digital-Beschleunigung-der-Schwerkraft-Neigung/dp/B0GDV9BKW3/ref=asc_df_B0GDV9BKW3?mcid=6cfbaf32e3ba3cecb27fd44287ff7af3&th=1&psc=1&tag=googshopde-21&linkCode=df0&hvadid=696222516891&hvpos=&hvnetw=g&hvrand=2182439717997627744&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9042022&hvtargid=pla-2478177908819&psc=1&hvocijid=2182439717997627744-B0GDV9BKW3-&hvexpln=0 , alibaba <1,00€
3. Выбрать Digitaler Drehzahlmesser в более нейтральном корпусе или перенести в другой корпус и добавить bluetooth. ChatGPT предлагает переделать готовый Digitaler Drehzahlmesser

### Простейшая система, которую можно будет развивать
1. 2x ADXL345 - 1,65 bei https://www.amazon.de/ADXL345-3-Achsen-Digital-Beschleunigung-der-Schwerkraft-Neigung/dp/B0GDV9BKW3/ref=asc_df_B0GDV9BKW3?mcid=6cfbaf32e3ba3cecb27fd44287ff7af3&th=1&psc=1&tag=googshopde-21&linkCode=df0&hvadid=696222516891&hvpos=&hvnetw=g&hvrand=12898539370183769966&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9042022&hvtargid=pla-2478177908819&psc=1&hvocijid=12898539370183769966-B0GDV9BKW3-&hvexpln=0 - заказал

2. 1x плата тахо (переделать готовый Digitaler Drehzahlmesser, для начала SEAFRONT HS2234 чтобы не было сюрпризов) - заказал.

3. 1x ESP32, у меня есть.

4. Провод - Cat5e, 6e STP(! экранированный) гибкий называется hochflexibles, schleppkettenfähiges Ethernet-Kabel

### Доработанная простейшая схема
У каждого датчика свой ESP32, в который приходит ещё и тахо.
Тахо также поставляет по этому кабелю питание.
Каждый ESP32 передаёт обработанную информацию дальше.
Тогда легко менять количество плоскостей.
Для уменьшения влияния датчика на измерения, датчик может отстыкавываться от ESP32. При этом также уменьшаются вибрационные нагрузки на ESP32.

# Самодельный станок для мини-турбин с точностью до 1 мг на ADXL335/BMI160+ESP32 с кодом
Самодельный станок в рамках проекта создания турбины. Очень качественные видео. Автор проекта с многолетним опытом (>40 лет был engineer in the Space Industry)
https://www.youtube.com/watch?v=dkPkfLmtImY - BMI160 accelerometer vs ADXL335
https://www.youtube.com/watch?v=KMYbToyST1M - 2x BMI160 accelerometer + ESP32
https://hackaday.com/2026/01/25/balancing-a-turbine-rotor-to-1-mg-with-a-diy-dynamic-balancer/
https://www.youtube.com/watch?v=oMzTQzkCGVw

# Теория (параллельный текст англ/нем)
rotor10.pdf (https://venghaus.eu/skripte/rotor10.pdf)

