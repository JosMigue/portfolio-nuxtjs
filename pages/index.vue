<template>
  <div>
    <Header/>
    <div class="ml-72 max-h-screen overflow-y-scroll overflow-x-hidden">
      <div class="bg-gray-100">
        <div class="grid lg:grid-cols-2 grid-cols-1 gap-2 p-20">
          <div>
            <h1 :class="`font-bold text-3xl text-dark`">José Miguel Galván</h1>
            <h3 :class="`mb-4 text-${$store.state.theme.secondaryfontcolor}-500`">Full-Stack Developer</h3>
            <p :class="`mb-4 text-${$store.state.theme.secondaryfontcolor}-700`">I'm a Full-Stack Developer, I really enjoy typing and solving complex problems in any porject that I'm assigned.</p>
            <div class="flex gap-4">
              <button type="button" class="py-2 px-5 rounded-md bg-blue-500 text-white font-bold hover:cursor-pointer"><font-awesome-icon class="mx-2" :icon="['fas', 'arrow-alt-circle-right']"/>View Portfolio</button>  
              <button type="button" class="py-2 px-5 rounded-md bg-gray-500 text-white font-bold hover:cursor-pointer"><font-awesome-icon class="mx-2" :icon="['fas', 'file-alt']"/>View Resume</button>  
            </div>       
          </div>
          <div>
            <img src="" alt="Photo">
          </div>
        </div>
      </div>
      <div>
        <div class="p-20">
          <div>
            <SectionTitle>What I Do</SectionTitle>
            <p class="text-justify text-md text-gray-600 mt-3">
              I have more than 2 years' experience building web apps. Below is a quick overview of my main technical skill sets and technologies I use. Want to find out more about my experience? Check out my online resume and project portfolio.
            </p>
          </div>
          <div class="mt-10">
            <div class="grid lg:grid-cols-4 grid-cols-2 gap-8">
              <div>
                <SectionSkillsSquare :icons="[{'prefix':'fab','class':'js-square','color':'yellow-300'}]">
                  Vainilla JavaScript
                  <template #resume>
                   I have worked with Vainilla JavaScript for more than 2 years, always taking in mind all good practices when using this wonderful technlogy.
                  </template>
                </SectionSkillsSquare>
              </div>
              <div>
                <SectionSkillsSquare :icons="[{'prefix':'fab','class':'vuejs','color':'green-400'}]">
                  Vue.js, Nuxt.js
                  <template #resume>
                    I learned this thecnology by mi self then I had the opportunity to work with many project using it as alternative of Jquery.
                  </template>
                </SectionSkillsSquare>
              </div>
              <div>
                <SectionSkillsSquare :icons="[{'prefix':'fab','class':'laravel','color':'yellow-700'},{'prefix':'fab','class':'php','color':'purple-400'}]">
                  Laravel, Livewire
                  <template #resume>
                    My first framework that I learned by myself, I love working with this technology, it is very easy to learn and use. I've been working during more that 2 years with this framework. 
                  </template>
                </SectionSkillsSquare>
              </div>
              <div>
                <SectionSkillsSquare :icons="[{'prefix':'fab','class':'python','color':'blue-300'}]">
                  Python
                  <template #resume>
                    I had the opportunity to work and learn this technology some time, but that time was enought to fall in love with it. 
                  </template>
                </SectionSkillsSquare>
              </div>
              <div>
                <SectionSkillsSquare :icons="[{'prefix':'fab','class':'npm','color':'red-400'},{'prefix':'fab','class':'yarn','color':'blue-500'}]">
                  npm, yarn
                  <template #resume>
                    In all my projects I use npm or yarn for my packages management.
                  </template>
                </SectionSkillsSquare>
              </div>
              <div>
                <SectionSkillsSquare :icons="[{'prefix':'fab','class':'css3-alt','color':'blue-400'},{'prefix':'fab','class':'html5','color':'yellow-600'}]">
                  CSS, HTML5
                  <template #resume>
                    The Beginning of everything, those technologies made me to get in love with web development.
                  </template>
                </SectionSkillsSquare>
              </div>
              <div>
                <SectionSkillsSquare :icons="[{'prefix':'fab','class':'bootstrap','color':'purple-400'}]">
                  Bootstrap, TailwindCSS, Bulma
                  <template #resume>
                    My first CSS framework was Bootstrap, after all I found out Bulma and now with the release of Jetstream I fell in love of TailwindCSS.
                  </template>
                </SectionSkillsSquare>
              </div>
              <div>
                <SectionSkillsSquare :icons="[{'prefix':'fas','class':'terminal','color':'black'},{'prefix':'fab','class':'linux','color':'black'},{'prefix':'fab','class':'git-alt','color':'[#ea580c]'}]">
                  Command Lines
                  <template #resume>
                   I've been using git bash for version control, I learned to user linux terminal because in a job that I had to configure Debian for laravel apps  
                  </template>
                </SectionSkillsSquare>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
