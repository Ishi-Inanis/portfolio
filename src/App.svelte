<script>
  import Header from './lib/Header.svelte';
  import Section from './lib/Section.svelte';
  import Article from './lib/Article.svelte';
  import Badge from './lib/Badge.svelte';
  import Github from './lib/Github.svelte';
  import Gitlab from './lib/Gitlab.svelte';
  import Telegram from './lib/Telegram.svelte';
  import Teletype from './lib/Teletype.svelte';

  const skills = {
        main: [{
          name: 'Svelte',
          color: 'red'
        }, {
          name: 'TailwindCSS',
          color: 'sky'
        }, {
          name: 'Fastify',
          color: 'neutral'
        }, {
          name: 'PhpStorm',
          color: 'purple'
        }, {
          name: 'WebStorm',
          color: 'blue'
        }, {
          name: 'NeoVim',
          color: 'emerald'
        }, {
          name: 'Git',
          color: 'red'
        }, {
          name: 'Zsh',
          color: 'orange'
        }, {
          name: 'Tmux',
          color: 'emerald'
        }, {
          name: 'Fedora',
          color: 'blue'
        }],
        hard: {
          languages: [{
            name: 'JavaScript',
            color: 'yellow'
          }, {
            name: 'HTML',
            color: 'orange'
          }, {
            name: 'CSS',
            color: 'sky'
          }, {
            name: 'TypeScript',
            color: 'blue'
          }, {
            name: 'PHP',
            color: 'violet'
          }, {
            name: 'C++',
            color: 'blue'
          }, {
            name: 'C#',
            color: 'fuchsia'
          }, {
            name: 'Kotlin',
            color: 'purple'
          }, {
            name: 'Java',
            color: 'orange'
          }, {
            name: 'Rust',
            color: 'red'
          }, {
            name: 'Pascal',
            color: 'blue'
          }],
          technologies: [{
            name: 'Jest',
            color: 'rose'
          }, {
            name: 'Git',
            color: 'red'
          }, {
            name: 'Linux',
            color: 'amber'
          }, {
            name: 'Sass',
            color: 'pink'
          }, {
            name: 'Scss',
            color: 'pink'
          }, {
            name: 'Bootstrap',
            color: 'purple'
          }, {
            name: 'Vue.js',
            color: 'emerald'
          }, {
            name: 'TailwindCSS',
            color: 'sky'
          }, {
            name: 'Svelte',
            color: 'red'
          }, {
            name: 'React',
            color: 'cyan'
          }, {
            name: 'MySQL',
            color: 'teal'
          }, {
            name: 'Node.js',
            color: 'green'
          }, {
            name: 'PostgreSQL',
            color: 'blue'
          }, {
            name: 'Fastify',
            color: 'neutral'
          }, {
            name: 'Express',
            color: 'green'
          }, {
            name: 'WordPress',
            color: 'sky'
          }],
          patterns: [],
        },
        soft: [{
          name: 'Умею находить общий язык с командой',
          color: ''
        }, {
          name: 'Способен самообучаться',
          color: ''
        }],
        other: [],
        tools: [{
          name: 'PhpStorm',
          color: 'purple'
        }, {
          name: 'WebStorm',
          color: 'blue'
        }, {
          name: 'IntelliJ Idea',
          color: 'rose'
        }, {
          name: 'CLion',
          color: 'teal'
        }, {
          name: 'Visual Studio Code',
          color: 'sky'
        }, {
          name: 'Vim',
          color: 'lime'
        }, {
          name: 'NeoVim',
          color: 'emerald'
        }, {
          name: 'Docker',
          color: 'sky'
        }, {
          name: 'Podman',
          color: 'purple'
        }, {
          name: 'Zsh',
          color: 'orange'
        }, {
          name: 'Tmux',
          color: 'emerald'
        }]
      },
      education = {
        main: [{
          institution: 'Институт электронных и информационных систем',
          faculty: 'Информатика и вычислительная техника',
          specialty: 'Программное обеспечение вычислительной техники и автоматизированных систем',
          graduation: 2025
        }, {
          institution: 'Политехнический колледж Новгородского государственного университета имени Ярослава Мудрого',
          faculty: 'Программирование в компьютерных системах',
          specialty: 'Техник-программист',
          graduation: 2020
        }],
        additional: [{
          organization: 'ФГБОУ ВО "Новгородский государственный университет имени Ярослава Мудрого"',
          name: 'Корпоративная защита от внутренних угроз информационной безопасности с использованием современных DLP технологий',
          graduation: 2020
        }, {
          organization: 'ФГБОУ ВО "Новгородский государственный университет имени Ярослава Мудрого"',
          name: 'Оператор ЭВМ',
          graduation: 2018
        }]
      },
      experience = [{
        company: 'Политехнический колледж Новгородского государственного университета имени Ярослава Мудрого',
        position: 'Преподаватель',
        begin: 'Сентябрь 2020',
        end: 'по настоящее время',
        description: 'Преподаватель по дисциплинам:\n' +
            'Проектирование и разработка веб-приложений;\n' +
            'Интернет технологии и публикация данных в сети Интернет;\n' +
            'Технология разработки и защиты баз данных;\n' +
            'Основы программирования;\n' +
            'Машинное обучение и большие данные;\n' +
            'Разработка мобильных приложений;\n' +
            'Разработка кода информационных систем;\n' +
            'Основы проектирования и разработки информационных систем.'
      }, {
        company: 'ООО "Сириус.ИС"',
        position: 'Младший разработчик программного обеспечения',
        begin: 'Август 2021',
        end: 'Июнь 2022',
        description: 'Frontend разработка на JS, React с Ant Design.\n' +
            'Backend разработка на Java и Apache Tomcat.'
      }],
      books = [{
        name: 'Чистая архитектура. Искусство разработки программного обеспечения',
        author: 'Роберт Мартин'
      }],
      languages = [
        'Русский — Родной',
        'Английский — A2 — Элементарный'
      ];
</script>

<Header avatar="/avatar.jpg">
  <span slot="name">Алексеев Пётр Сергеевич</span>
  <span slot="desc">Full stack developer</span>
  <a class="block text-blue-500" href="mailto:alexeev.dauwalter@gmail.com">alexeev.dauwalter@gmail.com</a>
  <nav class="flex flex-wrap gap-8 justify-center items-center">
    <a class="block dark:invert text-blue-500 w-10 h-10"
       href="https://github.com/ishi-inanis">
      <Github/>
    </a>
    <a class="block text-blue-500 w-10 h-10" href="https://gitlab.com/ishi-inanis">
      <Gitlab/>
    </a>
    <a class="block text-blue-500 w-10 h-10" href="https://t.me/alexeev_dauwalter">
      <Telegram/>
    </a>
  </nav>
</Header>

<main class="space-y-2 sm:space-y-6">
  <Section title="Обо мне">
    <p>Программирование для меня и хобби, и работа. В основном использую Linux. Имею опыт коммерческой разработки на
      PHP, JS, React и Java, а также опыт преподавания. Умею руководить командой и сопровождать проекты. Я
      коммуникабельный и стремлюсь стать частью дружной профессиональной команды, в которой смогу расти как
      специалист.</p>
    <p>Начинал работать на PHP, чаще всего с применением CMS Bitrix и Wordpress, но постепенно перешёл на разработку на
      JS. Также изучал C++, C#, Rust, Java и Kotlin.</p>
  </Section>

  {#if skills.main?.length}
    <Section title="Основной стек">
      <section class="flex flex-wrap gap-2 justify-center">
        {#each skills.main as { name, color }}
          {#if name}
            <Badge {name} {color}/>
          {/if}
        {/each}
      </section>
    </Section>
  {/if}

  {#if skills.hard || skills.soft || skills.tools || skills.other}
    <Section title="Ключевые навыки">
      {#if skills.hard?.languages.length}
        <Article title="Языки программирования">
          <section class="flex flex-wrap gap-2 justify-center">
            {#each skills.hard.languages as { name, color }}
              {#if name}
                <Badge {name} {color}/>
              {/if}
            {/each}
          </section>
        </Article>
      {/if}

      {#if skills.hard?.technologies.length}
        <Article title="Технологии">
          <section class="flex flex-wrap gap-2 justify-center">
            {#each skills.hard.technologies as { name, color }}
              {#if name}
                <Badge {name} {color}/>
              {/if}
            {/each}
          </section>
        </Article>
      {/if}

      {#if skills.hard?.patterns.length}
        <Article title="Паттерны">
          <section class="flex flex-wrap gap-2 justify-center">
            {#each skills.hard.patterns as { name, color }}
              {#if name}
                <Badge {name} {color}/>
              {/if}
            {/each}
          </section>
        </Article>
      {/if}

      {#if skills.tools?.length}
        <Article title="Инструменты">
          <section class="flex flex-wrap gap-2 justify-center">
            {#each skills.tools as { name, color }}
              {#if name}
                <Badge {name} {color}/>
              {/if}
            {/each}
          </section>
        </Article>
      {/if}

      {#if skills.soft?.length}
        <Article title="Гибкие навыки">
          <section class="flex flex-wrap gap-2 justify-center">
            {#each skills.soft as { name }}
              {#if name}
                <Badge {name}/>
              {/if}
            {/each}
          </section>
        </Article>
      {/if}

      {#if skills.other?.length}
        <Article title="Другое">
          <section class="flex flex-wrap gap-2 justify-center">
            {#each skills.other as { name }}
              {#if name}
                <Badge {name}/>
              {/if}
            {/each}
          </section>
        </Article>
      {/if}
    </Section>
  {/if}

  {#if experience?.length}
    <Section title="Опыт работы">
      {#each experience as { company, position, begin, end, description }}
        {#if company}
          <Article title={company}>
            {#if position}
              <p><strong>{position}</strong></p>
            {/if}
            {#if description}
              <p class="space-y-1">
                {#each description.split('\n') as row}
                  <p>{row}</p>
                {/each}
              </p>
            {/if}
            {#if begin && end}
              <p class="text-sm">{begin} — {end}</p>
            {/if}
          </Article>
        {/if}
      {/each}
    </Section>
  {/if}

  {#if education.main?.length}
    <Section title="Образование">
      {#each education.main as { institution, faculty, specialty, graduation }}
        {#if institution && faculty && specialty}
          <Article title={institution}>
            <p>{faculty}, <strong>{specialty}</strong></p>
            {#if graduation}
              <time class="block text-sm">{graduation}</time>
            {/if}
          </Article>
        {/if}
      {/each}
    </Section>
  {/if}

  {#if education.additional?.length}
    <Section title="Повышение квалификации">
      {#each education.additional as { organization, name, graduation }}
        {#if organization && name}
          <Article title={organization}>
            <p>{name}</p>
            {#if graduation}
              <time class="block text-sm">{graduation}</time>
            {/if}
          </Article>
        {/if}
      {/each}
    </Section>
  {/if}

  {#if languages?.length}
    <Section title="Знание языков">
      <section class="flex flex-wrap gap-2">
        {#each languages as name}
          {#if name}
            <Badge {name}></Badge>
          {/if}
        {/each}
      </section>
    </Section>
  {/if}

  {#if books?.length}
    <Section title="Прочитано">
      {#each books as { name, author }}
        {#if name && author}
          <Article title={name}>
            <address class="text-sm">{author}</address>
          </Article>
        {/if}
      {/each}
    </Section>
  {/if}

  <Section title="Дополнительные ссылки">
    <a class="block" href="https://teletype.in/@alexeev.dauwalter">
      <Teletype/>
    </a>
  </Section>
</main>