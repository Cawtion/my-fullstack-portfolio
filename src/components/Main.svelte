<script>
	import Step from "./Step.svelte";

  let steps = [
    {name: 'The Game Lab', description: 'Something is supposed to go here....hmm.', icon: 'fa-solid fa-dice-d6' },
    {name: 'My Projects', description: 'Comng soon...', icon: 'fa-brands fa-fantasy-flight-games' },
    {name: 'Candle Cove', description: 'I swear...', icon:'fa-solid fa-dice-d20' }
  ];

  let benefits = [
    {name: 'A Self Taught Developer', description: 'Fell in love with programming at a young age. I have the luxury of being able to approach projects from an unconventional lane. I studied all the free courses I could get my hands on. I started simple with HTML, CSS and Javascript, then stumbled my way into React. From there I learned Next.js and Svelte. Then I moved onto backend with Node.js, Express and MongoDB, NeonDB and Firebase, and now PostgreSQL.'},
    {name: 'Lover of Design and UX', description: 'I want to create a feeling when someone uses something I built. I use frontend tools like Figma to prototype, design and test user experiences before I start coding. I want to make sure that what I build is intuitive, easy to use and visually appealing.'},
    {name: 'An Excellent Problem Solver', description: 'I love this. Every project has its challenges, and I enjoy the process of breaking down problems, researching solutions, and implementing fixes. Whether it is debugging code or optimizing performance, I approach each challenge with a positive mindset and a determination to find the best solution.'},
  ]

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="flex flex-col items-center justify-start min-h-[calc(100vh-100px)] gap-10 py-8 sm:py-14">
        <div class="flex flex-col items-center justify-center text-center gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Cory</span> Williams <br/>Full Stack
                <span class="poppins text-violet-400">Developer</span>
            </h2>

            <p class="text-base sm:text-lg md:text-xl">
              My <span class="text-violet-400">favorite tech</span> includes Javascript (Next.js or Sveltekit),
            Tailwind CSS, Node.js, Express.js and PostgreSQL
            </p>
           <a 
   class="blueShadow mx-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
   href="https://www.linkedin.com/in/corywilliams984"
   target="_blank"
   aria-label="Visit my LinkedIn profile"
          >
   <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
   <h4 class="relative z-10">Get in touch &rarr;</h4>
   </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
          <img src={"images/FB_IMG_1759898817280~2.png"} alt="" class="object-cover z-2 max-h-[40vh]"/>
        </div>
      </section>
      <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
          <h6 class="text-large sm:text-xl md:text-2xl">
            Some of My Recent Projects
          </h6>
          <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Curious to <span class="poppins text-violet-400">see</span> my work?
          </h3>
          
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
             <Step step={steps[0]}>
               <p>The Game Lab is a hub for free games I've created along with some past time favorites.</p>
               <strong class="text-violet-400">Created with Phaser (Javascript framework)</strong>
             </Step>
              <Step step={steps[1]}>
                <p>Well, just like the title says, these are some of my projects</p>
                <strong class="text-violet-400">Let me know what you think!</strong>
              </Step>
              <Step step={steps[2]}>
                <p>Candle Cove is a hub for creepypastas and other stories that I like.</p>
                <strong class="text-violet-400">Feel free to submit your own!</strong>
              </Step>
        </div>
      </section>
      <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16
      sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-4 text-center relative before:absolute before:top-0
        before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0
        after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
          <h6 class="text-lg sm:text:xl md:text-2xl">Want to know more?</h6>
          <h3 class="font-semibold text 3-xl sm:text-4xl md:text-5xl">
              A bit <span class="poppins text-violet-400">about</span> me.
          </h3>
        </div>
        <p class="mx-auto font-semibold text-lg sm:text-xl md:text-2xl">I am...</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
             {#each benefits as benefit, index}
             <div class="flex gap-6 sm:gap-8">
              <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500
              font-semibold">
                 0{index+1}
            </p>
             <div class="flex flex-col gap-6 sm:gap-8">
                <h3 class="text-2xl sm:text-3xl md:text-5xl">
                  {benefit.name}
                </h3>

                <p>{benefit.description}</p>

             </div>
              </div>
             {/each}
        </div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-400 poppins">Complete</span> Package</h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
          <table class="bg-white text-slate-700 rounded text-center">
            <thead class="border-b border-solid border-slate-200">
              <tr class="">
                <th/>
                <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">Me</th>
                
              </tr>
            </thead>
            <tbody>
              <tr class="border-b border-solid border-slate-200">
                <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                text-sm whitespace-nowrap">Dedication</td>
                <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
                <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
              </tr>
                <tr class="border-b border-solid border-slate-200">
                <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                text-sm whitespace-nowrap">Critical Thinking</td>
                <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
              </tr>  
              <tr class="border-b border-solid border-slate-200">
                <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                text-sm whitespace-nowrap">Communication Skills</td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
                <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
              </tr>  
              <tr class="border-b border-solid border-slate-200">
                <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                text-sm whitespace-nowrap">Programming Ability</td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
                <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
                <td><i class="fa-solid fa-check text-slate-500"></i></td>
              </tr>  
            </tbody>
          </table>
        </div>
        <div class="mx-auto -m-12 italic sm:hidden opacity-50">
          <p>Scroll to see mor r&rr</p>
        </div>
        <p class="mx-auto">So why not invest?</p>
      </section>
</main>