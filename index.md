<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>{{ page.title | default: site.title }}</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      color: #373737;
      font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
      font-size: 16px;
      line-height: 1.5;
    }
    .wrapper { max-width: 960px; margin: 0 auto; }
    header {
      width: 270px;
      position: fixed;
      top: 0;
      left: 0;
      height: 100vh;
      padding: 48px 24px;
      text-align: center;
      overflow-y: auto;
      border-right: 1px solid #eee;
    }
    header img {
      width: 160px;
      height: 160px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 20px;
    }
    header h1 { font-size: 22px; margin: 0 0 8px; }
    header p { font-size: 15px; color: #555; margin: 4px 0; }
    section {
      margin-left: 300px;
      padding: 48px 40px;
      max-width: 640px;
    }
    @media (max-width: 800px) {
      header { position: static; width: auto; height: auto; border-right: none; border-bottom: 1px solid #eee; }
      section { margin-left: 0; }
    }
  </style>
</head>
<body>
  <div class="wrapper">
    <header>
      <img src="{{ site.author_photo }}" alt="{{ site.author_name }}">
      <h1>{{ site.author_name }}</h1>
      <p>{{ site.author_title }}</p>
      <p>{{ site.author_department }}</p>
      <p>{{ site.author_university }}</p>
    </header>
    <section>
      {{ content }}
    </section>
  </div>
</body>
</html>
