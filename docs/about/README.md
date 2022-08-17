---
pageClass: about-page
description: 'The biography and information about me.'
avatar: /profile.jpg
head: 'Zhaopeng Qiu'
info: 'Researcher at Tencent Jarvis Lab'
interests: 'Interests: Recommendation, .'
socials:
- title: github
  link: https://github.com/zpqiu
- title: email
  link: 'mailto:zhaopengqiu[at]tencent.com'
actions:
- text: Projects
  link: /projects/
- text: Blog
  link: https://github.com/mtobeiyf
- text: CV
  link: /article/
footer: Made with ♥ by Zhaopeng Qiu. Powered by VuePress
---

<AboutCard :frontmatter="$page.frontmatter" >

I attended [Hogwarts School of Witchcraft and Wizardry](https://en.wikipedia.org/wiki/Hogwarts) to study witchcraft, supervised by **Dumbledore** and other professors. I'm trying my best to battle with Lord Voldemort, the evil Wizard that we all fear. My research area includes Defence Against the Dark Arts and other magic. :dizzy:

</AboutCard>

<style lang="stylus">

.theme-container.about-page .page
  background-color #e6ecf0
  min-height calc(100vh)
  
  .last-updated
    display none

</style>