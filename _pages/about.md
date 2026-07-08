---
layout: about
title: about
permalink: /
subtitle: Information Systems student and researcher.

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>L.N. Gumilyov Eurasian National University</p>
    <p>Astana, Kazakhstan</p>
    <p>iskakovk2016@gmail.com</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true
  limit: 3
---

<style>
  /* Explicit, so a theme rule like `div { display: block }` can't defeat [hidden]. */
  #about-en[hidden],
  #about-ru[hidden] {
    display: none;
  }
</style>

<button id="lang-toggle" type="button" data-lang="en" aria-controls="about-en about-ru" style="margin-bottom: 1rem; cursor: pointer; padding: 0.3rem 0.75rem; border-radius: 0.35rem; border: 1px solid currentColor; background: transparent; color: inherit; font: inherit; font-size: 0.85rem;">
  Русский
</button>

<div id="about-en" markdown="1">

- **Information Systems undergraduate** at the Faculty of Information Technologies, L.N. Gumilyov Eurasian National University (GPA 3.92).
- **Machine Learning Tutor** at ITECHRESEARCH, where I develop curriculum and mentor more than 30 students; previously a Junior Research Assistant at the Eurasian National University.
- **Published research** in econometric modeling, exchange-rate forecasting, and natural language processing for the Kazakh language.
- **Awards:** recipient of the Presidential Scholarship of the Republic of Kazakhstan and the ENU Endowment Fund scholarship in the Young Researcher category.
- **Open to collaboration** on projects and research in machine learning and AI — the best way to reach me is by email.

</div>

<div id="about-ru" markdown="1" hidden>

- **Студент бакалавриата по специальности «Информационные системы»** на факультете информационных технологий Евразийского национального университета имени Л.Н. Гумилёва (GPA 3.92).
- **Преподаватель машинного обучения** в ITECHRESEARCH: разрабатываю учебную программу и курирую более 30 студентов; ранее — младший научный сотрудник Евразийского национального университета.
- **Публикации** по эконометрическому моделированию, прогнозированию обменного курса и обработке естественного языка для казахского языка.
- **Награды:** стипендиат Президентской стипендии Республики Казахстан и стипендии Эндаумент-фонда ЕНУ в номинации «Молодой исследователь».
- **Открыт к сотрудничеству** по проектам и исследованиям в области машинного обучения и ИИ — лучший способ связаться со мной по электронной почте.

</div>

<script>
  (function () {
    var btn = document.getElementById("lang-toggle");
    var en = document.getElementById("about-en");
    var ru = document.getElementById("about-ru");
    if (!btn || !en || !ru) return;

    // The subtitle is rendered by the theme layout, outside this page's content.
    var subtitle = document.querySelector(".post-description, p.desc");
    var subtitleText = {
      en: subtitle ? subtitle.textContent.trim() : "",
      ru: "Студент и исследователь в области информационных систем.",
    };

    function apply(lang) {
      var toRu = lang === "ru";
      en.hidden = toRu;
      ru.hidden = !toRu;
      btn.dataset.lang = lang;
      btn.textContent = toRu ? "English" : "Русский";
      if (subtitle) subtitle.textContent = subtitleText[lang];
      document.documentElement.lang = lang;
      try {
        localStorage.setItem("about-lang", lang);
      } catch (e) {
        /* storage unavailable (private mode) — toggle still works per-visit */
      }
    }

    var saved;
    try {
      saved = localStorage.getItem("about-lang");
    } catch (e) {
      saved = null;
    }
    if (saved === "ru") apply("ru");

    btn.addEventListener("click", function () {
      apply(btn.dataset.lang === "ru" ? "en" : "ru");
    });
  })();
</script>
