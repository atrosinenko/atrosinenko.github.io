---
layout: default
---

[In English](https://atrosinenko.github.io/)

Меня зовут Анатолий Тросиненко, и я Scala-программист. Но это официально, а по факту я изучаю всё, до чего дотянусь &mdash; фаззинг, инструментация кода, разработка средств разработки, даже немного процессоростроения на Chisel HDL &mdash; иногда в неожиданных комбинациях.

Сферы моих интересов:
* системное программирование и фаззинг (Linux kernel и другой open source): примерный список найденных багов в ядре, а точнее &mdash; коммитов, в которых я упомянут, [можно посмотреть здесь](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/log/?qt=grep&q=anatoly.trosinenko%40gmail.com). Есть даже несколько исправлений лично от Линуса Торвальдса &mdash; вот, что значит &laquo;вовремя отправить баг-репорт&raquo;
* инструментация кода: [динамическая](https://github.com/atrosinenko/qinst), [статическая](https://github.com/atrosinenko/llinst) -- есть даже [вшиваемая в RISC-V софт-процессор](https://github.com/atrosinenko/simpleinst) &mdash; все они имеют примерно похожий интерфейс (в идеале он должен стать [полностью идентичным](https://github.com/atrosinenko/bpfinst-spec)). В API сделан упор на максимальную похожесть реального инструментатора на псевдокод на C
* создание инструментов разработки
  * модуль поддержки Modelica, [вошедший в PMD 6.21.0](https://github.com/pmd/pmd/releases/tag/pmd_releases%2F6.21.0)
  * надстройка над PMD для минимизации исходников при сохранении инварианта &mdash; сослана в [отдельный репозиторий](https://github.com/pmd/pmd-scm) ментейнерами PMD
  * допиливание OpenModelica и конкретно её IDE OMEdit &mdash; в итоге задачу по реализации code completion ~торжественно~ повесили на выданный мне аккаунт на трекере
* Chisel HDL (это DSL для разработки оборудования на Scala)
  * преимущественно, эксперименты с RocketChip RISC-V soft-processor, в частности, [поддержка описания простых инструкций](https://github.com/atrosinenko/simple-inst) процессора на C
* портирование чего попало куда попало _и вообще_
  * портирование QEMU на JavaScript для реализации Proof-of-Concept трансляции машинного кода в [JS](https://habr.com/ru/post/315770/), а впоследствии и в [WebAssembly](https://habr.com/ru/post/451306/)
  * [портирование MemTest86+ на RISC-V](https://github.com/atrosinenko/memtest86-plus-riscv)

Многое из этого описано в моих [статьях на Хабре](https://habr.com/ru/users/atrosinenko/posts) и [выложено на Гитхабе](https://github.com/atrosinenko).

А ещё я как раз ищу работу: вот мои резюме [на русском](https://spb.hh.ru/resume/4465d3f7ff073190f10039ed1f6d4879656839) и [на английском](https://spb.hh.ru/resume/c7464acdff07c49ff30039ed1f38756f75424f).
