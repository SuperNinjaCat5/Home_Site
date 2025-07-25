

<svelte:head>
  <title>SuperNinjaCat5.us</title>
  <link rel="stylesheet" href="/fonts.css" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400..900&display=swap" rel="stylesheet">
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
</style>

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
      <p style="max-width: 80%; color: #00ff22; background-color: #001a00; padding: 1.5rem 2rem; border-radius: 12px; box-shadow: 0 0 15px #00ff22aa; font-family: 'Orbitron', sans-serif; font-size: 1.1rem; line-height: 1.6; border: 1.5px solid #00ff22;">
        Hi, I'm @SuperNinjaCat5<br>
        <br>
        - 🐍 Am speak Python and English  <br>
        - 🔥 Proud vibe coder  <br>
        - 🎮 Big fan of video games <br> 
        - 🐱 Unbiasedly believes cats are the best animals <br>  
        - Plays 🎺 but big and long  <br>
        <br>
        ---<br>
        <br>
        About Me <br>
        <br>
        I'm passionate about coding and gaming, I enjoy learning useless things (3.141592653589793238462643383279502). Currently focused on Python projects and getting free stuff from hcb lol.
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
        Get in Touch<br><br>
        📫 How to reach me: contact@superninjacat5.us
        <br><br>
        ---
      </p>
    </div>
</div>
