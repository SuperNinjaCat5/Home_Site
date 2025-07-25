<svelte:head>
  <title>SuperNinjaCat5.us</title>
  <link rel="stylesheet" href="/fonts.css" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400..900&display=swap" rel="stylesheet">
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no" />
</svelte:head>

<style>
    .glitch {
      animation: glitch 2s infinite;
    }

     @keyframes glitch {  /*Credit to https://github.com/hackclub/hackducky/blob/main/site/Current/src/index.css (hackducky ysws) cuz it inspired the site and I lifted this anim cuz i suck at anims :sob:*/
      0%, 100% { transform: translate(0); }
      20% { transform: translate(-2px, 2px); }
      40% { transform: translate(-2px, -2px); }
      60% { transform: translate(2px, 2px); }
      80% { transform: translate(2px, -2px); }
    }

    .background {
    background: #030303;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    z-index: -1;
  }

  @keyframes scrollLoop {
    0% { transform: translateX(0); }
    100% { transform: translateX(-50%); } /* changed from -100% */
  }

  .scroll-wrapper {
    overflow: hidden;
    width: 100vw;
    border: 2px solid lime;
    margin-top: 2rem;
    padding: 1rem 0; 
  }

  .scroll-content {
    display: flex;
    animation: scrollLoop 30s linear infinite;
    will-change: transform;
    white-space: nowrap;
  }

  .scroll-content p {
    display: inline-block;    
    min-width: 320px;        
    margin: 0 1rem;           
    padding: 1rem 1.5rem;    
    background-color: #001a00;
    color: #00ff22;
    border-radius: 12px;
    box-shadow: 0 0 8px #00ff2280;  
    border: 1.5px solid #00ff22;
    font-family: 'Orbitron', sans-serif;
    font-size: 1rem;         
    line-height: 1.6;
    white-space: normal;
    flex-shrink: 0;
    transition: transform 0.3s ease;  
  }

  .scroll-content p:hover {
  transform: scale(1.05);  
  }


</style>

<script lang=ts>
  let projects = [
    {
      link: "https://summer.hackclub.com/projects/4631",
      title: "Ear Trainer",
      desc: "Helps me recognize musical notes without googling sheet music.",
    },
    {
      link: "https://summer.hackclub.com/projects/7915",
      title: "Quackcer Backend",
      desc: "A script that lets you control a computer via Discord commands. :hackerman:",
    },
    {
      link: "https://summer.hackclub.com/projects/1117",
      title: "Terminal Tamagotchi",
      desc: "Take care of a pet in the terminal or it'll die",
    },
    {
      link: "https://summer.hackclub.com/projects/332",
      title: "Tic Tac Tkinter",
      desc: "A basic Python tic-tac-toe game with GUI.",
    },
    {
      link: "https://github.com/niiccoo2/city-gusser/",
      title: "City Guesser",
      desc: "Guess the city using AI blurbs and images.",
    },
    {
      link: "https://github.com/SuperNinjaCat5/SuperNinjaCat5",
      title: "Project ?",
      desc: "More to come soon :o",
    },
  ];
</script>

<div class="background"></div>

<div>
  <div style="display: flex; justify-content: center; margin-top: 2rem; overflow: hidden;">  <!-- SuperNinjaCat5.us title -->
    <svg viewBox="0 0 500 80" width="100%" preserveAspectRatio="xMidYMid meet" xmlns="http://www.w3.org/2000/svg" class="glitch">
        <defs>
          <filter id="neonGlow" x="-50%" y="-50%" width="200%" height="200%">
            <feDropShadow dx="0" dy="0" stdDeviation="3" flood-color="#00ff22" flood-opacity="0.8"/>
            <feDropShadow dx="0" dy="0" stdDeviation="5" flood-color="#00ff22" flood-opacity="0.6"/>
          </filter>
        </defs>
      <text x="250" y="50" font-family="Orbitron" fill="#00ff22" stroke="black" stroke-width="0" text-anchor="middle" dominant-baseline="middle">
        <tspan font-size="50" filter="url(#neonGlow)">SuperNinjaCat5</tspan>
        <tspan font-size="20" dy="-15" dx="5" stroke-width="0" filter="url(#neonGlow)">.us</tspan>
      </text>
    </svg>
  </div>
    <div style="display: flex; justify-content: center; margin-top: 2rem;">
      <p style="max-width: 80%; color: #00ff22; background-color: #001a00; padding: 1.5rem 2rem; border-radius: 12px; box-shadow: 0 0 15px #00ff22aa; font-family: 'Orbitron', sans-serif; font-size: 1.1rem; line-height: 1.6; border: 1.5px solid #00ff22; margin-bottom: 2rem;">
        Hi, I'm @SuperNinjaCat5<br>
        <br>
        - Am speak Python and <a href="https://www.youtube.com/watch?v=tbXfYeqLufY">English</a>  <br> <!--Easter Egg :o-->
        - Proud vibe coder  <br>
        - Big fan of video games <br> 
        - Unbiasedly believes cats are the best animals <br>  
        - <a href="/weazered">Plays 🎺 but big and long</a>  <br> <!--Easter Egg :o-->
        <br>
        ---<br>
        <br>
        About Me <br>
        <br>
        I'm passionate about coding and gaming, I enjoy learning useless things (3.141592653589793238462643383279502). Currently focused on Python projects and getting free stuff from hackclub lol.
        <br>
        ---
        <br>
        What I'm Working On
        <br>
        - Learning more advanced Python concepts<br>  
        - Building small games and tools  <br>
        <br>
        ---<br>
        <br>
        Get in <a href="/noway">Touch</a><br><br> <!--Easter Egg :o-->
        How to reach me: contact (at) superninjacat5.us
        <br><br>
        ---
      </p>
    </div>
    <div class="scroll-container">
      <div class="scroll-content" style="margin-bottom: 4rem; margin-top: 1rem;">
        {#each projects.concat(projects) as project}
          <a href={project.link} target="_blank" class="project-card"> <!--Why cant i just past <p> 1000 times :( i hate svelte-->
            <p><strong>{project.title}</strong><br />---<br />{project.desc}</p>
          </a>
        {/each}
      </div>
    </div>
    <footer>
      <p style="display: flex; justify-content: center; width: 100%; color: #00ff22; background-color: #001a00; padding: 1.5rem 2rem; border-radius: 12px 12px 0 0; box-shadow: 0 0 15px #00ff22aa; font-family: 'Orbitron', sans-serif; font-size: 1.1rem; line-height: 1.6; border: 1.5px solid #00ff22;">
        Made by <span class="hover:animate-bounce" style="margin-left: 0.35rem;">SuperNinjaCat5</span>!
      </p>
    </footer>
</div>