<script>
  
  import DoorStep from './DoorStep.svelte';

  import { 
    passPhrase,
    currentMDWxrd,
  } from './stores.js';

  import { getContext } from 'svelte';

  import PromptStartInvestigation from './PromptStartInvestigation.svelte';
  import PromptEnterPassPhrase from './PromptEnterPassPhrase.svelte';

  const { open } = getContext('simple-modal');

  const showPromptStartInvestigation = () => {
    open(PromptStartInvestigation);
  };

  const showPromptEnterPassPhrase = () => {
    open(PromptEnterPassPhrase);
  };

</script>

<svelte:head>
  <link href="https://fonts.googleapis.com/css?family=Knewave" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css?family=IM+Fell+DW+Pica" rel="stylesheet">
</svelte:head>

<div class='main'>

  <div class='header'>

    <h1 
      class='title'
      on:click={showPromptEnterPassPhrase}
    >
      Socratic Circle Home School
    </h1>

    <p class="tagline">
      Let's Talk About It
    </p>
  
  </div>

  <div class="pathFork">


    <div class="stepInStone">
      
      <p>Not sure where to begin? SCHS is a place where you can explore new learning in a sharing focused format. Any topic is a good topic if if interests you, start an adventure into something new...</p>

      <h2 
        class='stepInStone'
        on:click={showPromptStartInvestigation}
      >
        Start an Exploration
      </h2>

    </div>

    <div class="stepInStone">
      
      <p>
        "Success is stumbling from failure to failure with no loss of enthusiasm" -- Winston Churchill
      </p>

    </div>

    <div class="stepInStone">
      
      <p>Unsatisfied with the paths before you? (Write your own and become a trailblazer!)(TURN THESE INTO BUTTONS)</p>

    </div>

    <div class="stepInStone">
      
      <p>
        "You become what you give your attention to" -- Epictetus
      </p>

    </div>

    <div class="stepInStone">
      
      <p>Struggling with some challenge before you? (Ask a question to seek help from others)(TURN THESE INTO BUTTONS)</p>

    </div>

    <div class="stepInStone">
      
      <p>
        "Education is not something you can finish" -- Isaac Asimov
      </p>

    </div>

    <div class="stepInStone">
      
      <p>Interested in sharing your accumulated experiences? (Post up as a knowledge source for various areas you are familiar with)(TURN THESE INTO BUTTONS)</p>

    </div>


    <!-- TEMPLATE -->
    <!-- <div class="stepInStone">
      
      <p>
        REPLACE_THIS
      </p>

    </div> -->

    <div class="stepInStone">
      
      <p>
        "Try to learn something about everything and everything about something" -- Thomas Huxley
      </p>

    </div>

    <div class="stepInStone">
      
      <p>Don't see what you're looking for? Suggest a new Step In Stone Here(TURN THESE INTO BUTTONS)</p>

    </div>
  

  </div> 

  <div class="footer">

    <p>
      We open these doors with the intention of establishing a <a href="https://youtube.com/clip/Ugkx9MkejdusERb7h2scBMdzu41f5ijTO1WO">Success 3.0</a> institution.
    </p>

  </div>

</div>

<style>


  *, *:before, *:after {box-sizing:  border-box !important;}


  .pathFork {
    column-width: 13em;
    column-gap: 0.5em;
  }

  .stepInStone {
    display: inline-block;
    text-align: center;
    margin:  0.25rem;
    padding:  1rem;
    width:  100%; 
    border: 0.1em solid black;
    border-radius: 0.73rem;
  }




  /*  styles for background color, etc; not necessary for this thing to work  */




  .header {

    text-align: center;
  }

  .title {
    font-size:  3rem;
    font-weight:  800;
    font-family: 'IM Fell DW Pica';
    padding-bottom: 0px;
    margin: 0px;
  }

  .tagline {
    font-size: 2rem;
    font-weight: 200;
    font-family: 'Knewave';
    padding-bottom: 20px;
    padding-top: 10px;
    margin: 0px;
  }


  .footer {
    font-size: 1rem;
    font-weight: 200;
    padding-bottom: 20px;
    padding-top: 10px;
    margin: 0px;
    width: 100%;
    text-align: center;
  }







</style>