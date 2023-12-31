# Как потестить всё самому?

Запускаем всё по порядку в этом блокноте: [LlamaPG](https://colab.research.google.com/drive/1W2uXUYEFvVsX1iEG_vA6IJA8bn7mGAVy?usp=sharing)

Блокнот с SD, который непосредственно рисует (но его нельзя запускать в чистом виде, он банится колабом). Можно проигнорировать, если вам не обязательно получать иллюстрации: [Готовый вариант .ipynb блокнота с Counterfeit V3 Stable Diffusion](https://github.com/CodeDruidX/LLamaPG/blob/main/my_counterfeit_webui_colab.ipynb)

Штука, которая запускет блокнот со SD без блокировки (Если оно вам надо): [Запуск .ipynb без блокировок](https://colab.research.google.com/drive/134f2PLaWs8mSXVUyzMnrV3RyXQteXMi5?usp=sharing)

# Если вы оказались в этом репозитории случайно:

<a href="https://habr.com/ru/company/ruvds/blog/523004/"><img src="https://habrastorage.org/webt/xu/2h/va/xu2hvap392fmfb45wgzkwdpfjs8.png" align="center"></a>
Языковые модели (<a href="https://en.wikipedia.org/wiki/Natural_language_processing">NLP</a>) сейчас активно развиваются и находят себе всё больше <i>интересных</i> применений. Начиналась же их эпоха с классики жанра - <a href="https://ru.m.wikipedia.org/wiki/Dungeons_%26_Dragons">D&D</a>. Это настольная игра, где несколько друзей или просто знакомых синхронно <i>галлюцинируют</i>, предсталяя себя командой героев в неком <i>вымышленном</i> мире. Прав же во внутриигровых выборах тот, кто выкинул большее число на игральной кости. Судить сейчас об их мотивации у меня нет никакого желания, да и статья вообще-то не об этом.
Важно только понимать, что движущей силой сюжета в их сессиях является лишь один из игроков, называемый <a href="https://en.m.wikipedia.org/wiki/Dungeon_Master">Dungeon Master</a>.
Когда только начали появляться первые <a href="https://ru.m.wikipedia.org/wiki/Generative_pre-trained_transformer">GPT</a> модели, одной из первых хотелок гиков оказалось желаение сварить из нейросетей автоматического Dungeon Masterа.
Так и появился <a href="https://aidungeon.io/">AIDungeon</a> - уникальная для своего времени (2019 год) вещь, которая не сильно потеряла в популярности и по сей день.
Однако, если вы любите смотреть глубже, то играть в него вам быстро надоест. Я же в своей серии из нескольких статей (посвящённых <a href="https://ru.m.wikipedia.org/wiki/Generative_pre-trained_transformer">GPT</a>) я стараюсь показать простому обывателю механизм безболезненного использования нейросетевых моделей в простых проектах при помощи python и <a href="https://huggingface.co/docs/transformers/index">Hugging Face Transformers</a>
<cut text="Приступим"/>
Фактически, статья является логическим продолжением прошлой: <a href="https://habr.com/ru/articles/751972/">Реально Бесконечное (лето) RuGPT3.5: Генерация новеллы на ходу нейросетью</a>
В ней были получены достаточно спорные результаты: с одной стороны, она оставила после себя уникальный легаси для тренировки квантованных лор, с другой же, итоговый результат оказался едва ли удовлетворителен.
Да и "новелла" получилась совершенно не визуальной. А идея генерации сценария для <a href="https://www.renpy.org/">RenPY </a>и вовсе оказалась мертворождённой.

Тут я хотел бы учесть совершённые в прошлый раз ошибки и… переработать всё заново.
Сама статья обитает тут: https://habr.com/ru/companies/ruvds/articles/759226/
Репозиторий создан в качестве приложения к основной статье ввиде ссылок или готовых файлов для заупска.
