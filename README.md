# mkdocs-material-pwa-vercel.com

An MkDocs-Material project with a PWA, ready for deployment to Vercel

  

## Build Status

  

[![Build Status](https://travis-ci.org/russelltadams/mkdocs-material-pwa-vercel.com.svg?branch=master)](https://travis-ci.org/russelltadams/mkdocs-material-pwa-vercel.com ) ![.github/workflows/link-checker.yml](https://github.com/russelltadams/mkdocs-material-pwa-vercel.com/workflows/.github/workflows/link-checker.yml/badge.svg) - Master branch

[![Build Status](https://travis-ci.org/russelltadams/mkdocs-material-pwa-vercel.com.svg?branch=develop)](https://travis-ci.org/russelltadams/mkdocs-material-pwa-vercel.com ) ![.github/workflows/link-checker.yml](https://github.com/russelltadams/mkdocs-material-pwa-vercel.com/workflows/.github/workflows/link-checker.yml/badge.svg?branch=develop) - Develop branch

  
  
  

## What's the point?

  

Read [here](https://github.com/russelltadams/mkdocs-material-pwa-vercel.com/blob/master/docs/index.md) for some background what this is and why you might want to do it if you are not already familiar with the parts of this little stack.

  

* Mkdocs - Markdown to static html [http://mkdocs.org](http://mkdocs.org)

* Material theme for MkDocs - [https://squidfunk.github.io/mkdocs-material/](https://squidfunk.github.io/mkdocs-material/)

* PWA builder for helpful PWA bits - [https://www.pwabuilder.com/](https://www.pwabuilder.com/)

* Vercel serverless hosting - [https://vercel.com ](https://vercel.com )

  

### Demo Sites

  

[https://mkdocs-material-pwa-zeitco.russelltadams.now.sh/](https://mkdocs-material-pwa-zeitco.russelltadams.now.sh/) - master

[https://mkdocs-material-pwa-zeitco-git-develop.russelltadams.now.sh/](https://mkdocs-material-pwa-zeitco-git-develop.russelltadams.now.sh/) - develop

  

## Setup

  

Предполагается, что вы разветвили или скопировали `mkdocs-material-pwa-vercel.com ` в собственный репозиторий Github.

  

### Local Development

  

Последние последние версии Mkdocs вышли за рамки python 2.x и теперь требуют Python 3.5 и выше. Python 3.8.x работает отлично.

  

```shell

mkvirtualenv --python=`which python3` mkdocs

mkvirtualenv mkdocs

workon mkdocs

pip install -r requirements.txt

mkdocs serve

```

Использование виртуальной среды python является необязательным, но настоятельно рекомендуется.

  

If you can get through the above, solving any complaints you run into, you should end up with the local development server running. This is super cool as you can now make changes to you mkdocs setup (mkdocs.yml) or your content (the markdown docs in /docs) and the "web server" will load the changes live when you save the file. Open your browser to `http://127.0.0.1:8000/`.

  

Now while the server is running, and you have the home page open in the browser, make changes to and save `/docs/index.md`. The server should automatically reload and show your changes.

  

## vercel.com serverless hosting and Github integration

  

Get an account on [vercel.com ](https://vercel.com ). It's free, they currently do not ask for any CC information to get signed up, and the free account allows plenty of room for developing multiple apps, and even running them in production at small scales.

  

### Vercel Github Integration

  

Connect your Vercel account to your Github account following the instructions after logging into Vercel. Create a new project in Vercel pointing it at your copy of this repo in your Github account. By default your `master` branch in Github will be considered the production release, but commits to other branches like `develop` will be pulled and built to preview. You can of course change these setting if you desire.

  

### Next steps for Vercel fanciness

  

Setup a custom domain(s) attached to the desired branch(es). You will need to point your domain registrar towards Vercel DNS servers. Vercel will give you a list of DNS servers after you submit your domain in the project.

  

## Test the PWA

  

Простой способ протестировать биты PWA - использовать инструменты разработчика Google Chrome, встроенные в Chrome.

  

1. В Google Chrome перейдите по URL-адресу, который вы хотите проверить. Вы можете проверить любой URL-адрес в Интернете.

1. Откройте Chrome DevTools.

1. Перейдите на вкладку Аудиты.

1. Убедитесь, что выбран PWA, запустите аудиты

  

Это даст базовую проверку. DevTools может показать вам гораздо больше, если вы копаетесь вокруг.

  

## To-Do

  

* Объясните PWA bits (manifest, service worker, and supporting bits)

* Добавить несколько `Hipster Ipsum` к демонстрационному содержимому, чтобы продемонстрировать силу тема материала или сделать страницы достаточно длинными, чтобы в игру вступило оглавление

* Добавьте какое-либо уведомление или ссылку, чтобы пользователь знал, что вы можете установить PWA. У Chrome есть уведомление, если вы заметили это, но я не уверен, как другие браузеры справляются с этим, если вообще обрабатывают

  

## Contribute?

  

Да, пожалуйста. Если вы видите ошибку или что-то, что могло бы быть лучше, или у вас есть идея улучшить концепцию здесь, не стесняйтесь разветвлять, ветвить и PR или поднимать проблему. Спасибо!