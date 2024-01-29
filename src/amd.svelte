<script>

  import { navigate } from "svelte-routing";
  import { onMount } from "svelte";
  
  function goToCartPage(){
      saveConfiguration();
      navigate("/cart");
  }
  
  function goToHomePage(){
    saveConfiguration();
    navigate("/");
  }

  function saveConfiguration(){
    const configurationToSave = {
      selectedProcessor,
      selectedMotherboard,
      selectedGraphicsCard,
      selectedPowerSupply,
      selectedRam,
      selectedStorage,
      selectedCase,
      selectedScreen,
      selectedKeyboard,
      selectedMouse,
      selectedChair,
      selectedSpeakers,
      selectedMicrophone
    };
    localStorage.setItem("pcConfigurationAMD", JSON.stringify(configurationToSave));
  }
  
    let processors = [
      { name: 'AMD Ryzen 5', price: 200 },
      { name: 'AMD Ryzen 7', price: 300 },
      { name: 'AMD Ryzen 9', price: 400 }
    ];
  
    let motherboards = {
      'AMD Ryzen 5': [
        { name: 'Scheda madre A', price: 100 },
        { name: 'Scheda madre B', price: 120 }
      ],
      'AMD Ryzen 7': [
        { name: 'Scheda madre C', price: 150 },
        { name: 'Scheda madre D', price: 180 }
      ],
      'AMD Ryzen 9': [
        { name: 'Scheda madre E', price: 200 },
        { name: 'Scheda madre F', price: 220 }
      ]
    };
  
    let graphicsCards = [
      { name: 'NVIDIA GTX 1660', price: 250 },
      { name: 'NVIDIA RTX 3060', price: 400 },
      { name: 'AMD RX 5700', price: 350 }
    ];
  
    let powerSupplies = [
      { name: '500W', price: 50 },
      { name: '600W', price: 70 },
      { name: '750W', price: 90 }
    ];
  
    let ramOptions = [
      { name: '8GB', price: 80 },
      { name: '16GB', price: 120 },
      { name: '32GB', price: 200 }
    ];
  
    let storageOptions = [
      { name: 'SSD 256GB', price: 100 },
      { name: 'SSD 512GB', price: 150 },
      { name: 'HDD 1TB', price: 80 }
    ];
  
    let cases = [
      { name: 'Case 1', price: 60 },
      { name: 'Case 2', price: 80 },
      { name: 'Case 3', price: 100 }
    ];

  let screens = [
    { name: '23.8" MSI PRO MP2412', price: 96 },
    { name: 'MONITOR IPS DA 23,8 POLLICI PCS BD24', price: 98 },
    { name: 'AOC 23.8" 24B2XDAM', price: 119 },
    { name: 'AOC E2470SWH 23.6"23.8"', price: 120 },
    { name: 'IIYAMA PROLITE XU2793HS-B5 27"', price: 141 },
    { name: 'AOC 27" 27B2AM', price: 143 },
    { name: 'IIYAMA XUB2492HSU-B6', price: 151 },
    { name: 'ASUS TUF GAMING VG249Q1A 24"', price: 178 },
    { name: 'MONITOR CURVO AOC C24G2AE/BK 23,6"', price: 180 }
  ];

  let keyboards = [
    { name: 'TASTIERA USB LOGITECH K120', price: 17 },
    { name: 'COMBO WIRELESS LOGITECH MK270', price: 40 },
    { name: 'COMBO WIRELESS LOGITECH MK540', price: 69 },
    { name: 'TASTIERA PER GAMING CORSAIR K55 RGB PRO (IT)', price: 74 }
  ];

  let mice = [
    { name: 'MOUSE OTTICO A CONNESSIONE USB PCS M400', price: 5 },
    { name: 'MOUSE USB OTTICO LOGITECH®', price: 8 },
    { name: 'MOUSE PER GAMING ASUS TUF M3 GEN II', price: 21 },
    { name: 'MOUSE PER GAMING MM310 BIANCA', price: 28 },
    { name: 'RAZER® DEATHADDER ESSENTIAL', price: 23 },
    { name: 'MOUSE CABLATO STEELSERIES RIVAL 3', price: 41 },
    { name: 'IIYAMA XUB2492HSU-B6', price: 151 },
    { name: 'MOUSE PER GAMING MM730 - BIANCO', price: 46 },
    { name: 'MOUSE PER GAMING ASUS TUF GAMING M4 AIR', price: 51 }
  ];

  let gamingChairs = [
    { name: 'nero', price: 228 },
    { name: 'rosso', price: 228 },
    { name: 'grigio', price: 228 },
    { name: 'rosa', price: 228 },
    { name: 'teal', price: 228 },
    { name: 'ciliegio', price: 228 }
  ];

  let speakerSystems = [
    { name: 'CASSE LOGITECH Z200 2.0', price: 46 },
    { name: 'CASSE LOGITECH Z313 2.1', price: 56 },
    { name: 'CASSE LOGITECH Z333 2.1', price: 82 }
  ];

  let microphones = [
    { name: 'WEBCAM HD LOGITECH® C270', price: 31 },
    { name: 'WEBCAM ASUS C3', price: 61 },
    { name: 'WEBCAM LOGITECH® C920', price: 96 },
    { name: 'WEBCAM HD LOGITECH® C930E', price: 157 }
  ];
    
  let selectedProcessor = { name: '', price: 0 };
  let selectedMotherboard = { name: '', price: 0 };
  let selectedGraphicsCard = { name: '', price: 0 };
  let selectedPowerSupply = { name: '', price: 0 };
  let selectedRam = { name: '', price: 0 };
  let selectedStorage = { name: '', price: 0 };
  let selectedCase = { name: '', price: 0 };
  let selectedScreen = { name: '', price: 0 };
  let selectedKeyboard = { name: '', price: 0 };
  let selectedMouse = { name: '', price: 0 };
  let selectedChair = { name: '', price: 0 };
  let selectedSpeakers = { name: '', price: 0 };
  let selectedMicrophone = { name: '', price: 0 };

  onMount(() => {
    const savedConfiguration = JSON.parse(localStorage.getItem("pcConfigurationAMD")) || {};
    selectedProcessor = savedConfiguration.selectedProcessor || { name: '', price: 0 };
    selectedMotherboard = savedConfiguration.selectedMotherboard || { name: '', price: 0 };
    selectedGraphicsCard = savedConfiguration.selectedGraphicsCard || { name: '', price: 0 };
    selectedPowerSupply = savedConfiguration.selectedPowerSupply || { name: '', price: 0 };
    selectedRam = savedConfiguration.selectedRam || { name: '', price: 0 };
    selectedStorage = savedConfiguration.selectedStorage || { name: '', price: 0 };
    selectedCase = savedConfiguration.selectedCase || { name: '', price: 0 };
    selectedScreen = savedConfiguration.selectedScreen || { name: '', price: 0 };
    selectedKeyboard = savedConfiguration.selectedKeyboard || { name: '', price: 0 };
    selectedMouse = savedConfiguration.selectedMouse || { name: '', price: 0 };
    selectedChair = savedConfiguration.selectedChair || { name: '', price: 0 };
    selectedSpeakers = savedConfiguration.selectedSpeakers || { name: '', price: 0 };
    selectedMicrophone = savedConfiguration.selectedMicrophone || { name: '', price: 0 };
  });

    $: total = calculateTotal(selectedProcessor, selectedMotherboard, selectedGraphicsCard, selectedPowerSupply, selectedRam, selectedStorage, selectedCase, selectedScreen, selectedKeyboard, selectedMouse, selectedChair, selectedSpeakers, selectedMicrophone);
  
    function findPrice(component, componentArray, processorName) {
  if (processorName && component && component.name) {
    const motherboardsForProcessor = motherboards[processorName];
    if (motherboardsForProcessor) {
      const motherboard = motherboardsForProcessor.find(m => m.name === component.name);
      if (motherboard) {
        return motherboard.price;
      }
    }
  }

  if (component && component.name) {
    const foundComponent = componentArray.find(c => c.name === component.name);
    return foundComponent ? foundComponent.price : 0;
  }

  return 0;
}

function calculateTotal(selectedProcessor, selectedMotherboard, selectedGraphicsCard, selectedPowerSupply, selectedRam, selectedStorage, selectedCase, selectedScreen, selectedKeyboard, selectedMouse, selectedChair, selectedSpeakers, selectedMicrophone) {
    total = 0;
    total += findPrice(selectedProcessor, processors);
    total += findPrice(selectedMotherboard, [], selectedProcessor.name);
    total += findPrice(selectedGraphicsCard, graphicsCards);
    total += findPrice(selectedPowerSupply, powerSupplies);
    total += findPrice(selectedRam, ramOptions);
    total += findPrice(selectedStorage, storageOptions);
    total += findPrice(selectedCase, cases);
    total += findPrice(selectedScreen, screens);
    total += findPrice(selectedKeyboard, keyboards);
    total += findPrice(selectedMouse, mice);
    total += findPrice(selectedChair, gamingChairs);
    total += findPrice(selectedSpeakers, speakerSystems);
    total += findPrice(selectedMicrophone, microphones);
    return total;
  }
  </script>











<main>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <div class="div">
          <div class="div-123">
            <div class="div-124">
              <div class="div-125">
                <a href="/">
                  <button class="button" data-text="Awesome">
                    <span class="actual-text">&nbsp;IIS Castelli&nbsp;</span>
                    <span aria-hidden="true" class="hover-text">&nbsp;IIS Castelli&nbsp;</span>
                    <!-- svelte-ignore a11y-missing-content -->
                  </button>
                </a>
              </div>
              <div class="loader"></div>
              <div class="div-126">
                <div class="div-127">
                  <div>
                    <a href="https://www.iiscastelli.edu.it/Pager.aspx?Page=mainpage"><button class="btn"><i class="animation"></i>Chi Siamo<i class="animation"></i></button>
                    </a>
                    
                  </div>
                </div>
                <div class="div-128">
                  <div>
                      <button class="btn" ><i class="animation"></i>Recensioni<i class="animation"></i>
                      </button>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="div-129">
            <div class="div-130">
              
    
              <div class="div-2">
        <div class="div-3">
          <div class="div-4">Configura questo PC</div>
          <div class="div-5">
            <div class="div-6">
              <div class="div-7">
                <div class="div-8">Riepilogo sistema</div>
                <div class="div-9">
                  <p><strong>Totale: €{total}</strong></p>
                </div>
              </div>
              <div class="div-10">
                <button class="cssbuttons-io-button">
                  Procedi
                  <div class="icon">
                    <svg
                      height="24"
                      width="24"
                      viewBox="0 0 24 24"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path d="M0 0h24v24H0z" fill="none"></path>
                      <path
                        d="M16.172 11l-5.364-5.364 1.414-1.414L20 12l-7.778 7.778-1.414-1.414L16.172 13H4v-2z"
                        fill="currentColor"
                      ></path>
                    </svg>
                  </div>
                </button>
                
              </div>
            </div>
          </div>
        </div>
        <div class="div-11">
          <div class="div-12">
            <div class="div-13">1) seleziona un case</div>
            <div class="div-14">
<ul>
  <li> <img src="https://m.media-amazon.com/images/I/61lqvjiI6rL._AC_UL480_FMwebp_QL65_.jpg" alt="cut citrus fruits. " />31,90€</li>
  <li> <img src="https://m.media-amazon.com/images/I/812VDXM-6OL._AC_UL480_FMwebp_QL65_.jpg" alt="sliced mango. " />36,90€</li>
  <li> <img src="https://m.media-amazon.com/images/I/81XpcOm+j0L._AC_UL480_FMwebp_QL65_.jpg" alt="a bunch of blueberries. " />42,50€</li>
  <li> <img src="https://m.media-amazon.com/images/I/71SY9Em7gdL._AC_UL480_FMwebp_QL65_.jpg" alt="a pineapple sitting on a table. " />52,90€</li>
  <li> <img src="https://m.media-amazon.com/images/I/71X77cdoOML._AC_UL480_FMwebp_QL65_.jpg" alt="frozen raspberries. " /> 55,50€</li>
  <li> <img src="https://m.media-amazon.com/images/I/81bl1gMgrxL._AC_UL480_FMwebp_QL65_.jpg" alt="a sliced strawberry. " />62,50€</li>
  <li> <img src="https://m.media-amazon.com/images/I/716HjcllKNL._AC_UL480_FMwebp_QL65_.jpg" alt="an arrangement of assorted sliced fruits. " />67,16€ </li>
  <li> <img src="https://m.media-amazon.com/images/I/71JjBd-bh+L._AC_UL480_FMwebp_QL65_.jpg" alt="sliced watermelons. " />69,90€</li>
  <li> <img src="https://m.media-amazon.com/images/I/81VZo8hrKqL._AC_UL480_FMwebp_QL65_.jpg" alt="grapefruits, lemons, and pomegranates. " />74,90€ </li>
  <li> <img src="https://m.media-amazon.com/images/I/71bjij9F8vL._AC_UL480_FMwebp_QL65_.jpg" alt="half of an avocado. " />89,17€</li>
  <li> <img src="https://m.media-amazon.com/images/I/71s+qbMWMLL._AC_UL480_FMwebp_QL65_.jpg" alt="half of a lime. " />119,90€</li>
  <li> <img src="https://m.media-amazon.com/images/I/71oX0C219kL._AC_UL480_FMwebp_QL65_.jpg" alt="a single cherry with stem. " />129,90€</li>
  <li> <img src="https://m.media-amazon.com/images/I/71XvonFM2fL._AC_UL480_FMwebp_QL65_.jpg" alt="a bunch of bananas. " />129,00€</li>
  <li> <img src="https://m.media-amazon.com/images/I/61CTe9lywcL._AC_UL480_FMwebp_QL65_.jpg" alt="three pears. " />139,99€</li>
  <li> <img src="https://m.media-amazon.com/images/I/812Na8YY3mL._AC_UL480_FMwebp_QL65_.jpg" alt="a basket full of peaches next to a plate with sliced peaches. " />166,50€</li>
  <li> <img src="https://m.media-amazon.com/images/I/71E9OQzIZUL._AC_UL480_QL65_.jpg" alt="a bowl of avocados. " />167,94€</li>
</ul>
            </div>
            <div class="div-41">2) scegli i tuoi componenti core</div>
            <div class="div-42">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/900c3b4b8b4705dcf0c79340c085ef1cd20f1d9cd819ccc47f3b1b9b8492706e?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/900c3b4b8b4705dcf0c79340c085ef1cd20f1d9cd819ccc47f3b1b9b8492706e?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/900c3b4b8b4705dcf0c79340c085ef1cd20f1d9cd819ccc47f3b1b9b8492706e?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/900c3b4b8b4705dcf0c79340c085ef1cd20f1d9cd819ccc47f3b1b9b8492706e?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/900c3b4b8b4705dcf0c79340c085ef1cd20f1d9cd819ccc47f3b1b9b8492706e?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/900c3b4b8b4705dcf0c79340c085ef1cd20f1d9cd819ccc47f3b1b9b8492706e?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/900c3b4b8b4705dcf0c79340c085ef1cd20f1d9cd819ccc47f3b1b9b8492706e?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/900c3b4b8b4705dcf0c79340c085ef1cd20f1d9cd819ccc47f3b1b9b8492706e?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-15"
              />
              <div class="div-43">
                <div class="div-44">Processore (CPU)</div>
                <div class="div-45">
                  <div class="div-46">
                    <label>
                      Processore:
                      <select bind:value={selectedProcessor.name}>
                        {#each processors as processor}
                          {#if selectedProcessor.name == processor.name}
                            <option value={processor.name} selected>{processor.name} - €{processor.price}</option>
                          {:else}
                            <option value={processor.name} >{processor.name} - €{processor.price}</option>
                          {/if}
                        {/each}
                      </select>
                    </label>     
                  </div>
                </div>
              </div>
            </div>
            <div class="div-49">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/b2a8fd79f82fda03376622873c5db7618051bf2f039a36cc6fe79e67ed20cf05?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/b2a8fd79f82fda03376622873c5db7618051bf2f039a36cc6fe79e67ed20cf05?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/b2a8fd79f82fda03376622873c5db7618051bf2f039a36cc6fe79e67ed20cf05?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/b2a8fd79f82fda03376622873c5db7618051bf2f039a36cc6fe79e67ed20cf05?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/b2a8fd79f82fda03376622873c5db7618051bf2f039a36cc6fe79e67ed20cf05?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/b2a8fd79f82fda03376622873c5db7618051bf2f039a36cc6fe79e67ed20cf05?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/b2a8fd79f82fda03376622873c5db7618051bf2f039a36cc6fe79e67ed20cf05?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/b2a8fd79f82fda03376622873c5db7618051bf2f039a36cc6fe79e67ed20cf05?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-17"
              />
              <div class="div-50">
                <div class="div-51">Scheda madre</div>
                <div class="div-52">
                  <div class="div-53">
                    {#if selectedProcessor.name}
                      <label>
                        Scheda madre:
                        <select bind:value={selectedMotherboard.name}>
                          {#each motherboards[selectedProcessor.name] as motherboard}
                          {#if selectedMotherboard.name == motherboard.name}
                            <option value={motherboard.name} selected>{motherboard.name} - €{motherboard.price}</option>
                          {:else}
                            <option value={motherboard.name}>{motherboard.name} - €{motherboard.price}</option>
                          {/if}
                          {/each}
                        </select>
                      </label>
                    {/if} 
                  </div>
                </div>
              </div>
            </div>
            <div class="div-56">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/84b6e5d6c4835189f2165bf56d89fdae124a4633e857c977aff4319b106b99d1?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/84b6e5d6c4835189f2165bf56d89fdae124a4633e857c977aff4319b106b99d1?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/84b6e5d6c4835189f2165bf56d89fdae124a4633e857c977aff4319b106b99d1?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/84b6e5d6c4835189f2165bf56d89fdae124a4633e857c977aff4319b106b99d1?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/84b6e5d6c4835189f2165bf56d89fdae124a4633e857c977aff4319b106b99d1?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/84b6e5d6c4835189f2165bf56d89fdae124a4633e857c977aff4319b106b99d1?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/84b6e5d6c4835189f2165bf56d89fdae124a4633e857c977aff4319b106b99d1?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/84b6e5d6c4835189f2165bf56d89fdae124a4633e857c977aff4319b106b99d1?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-19"
              />
              <div class="div-57">
                <div class="div-58">Memoria (RAM)</div>
                <div class="div-59">
                  <div class="div-60">
                    <label>
                      RAM:
                      <select bind:value={selectedRam.name}>
                        {#each ramOptions as ramOption}
                        {#if selectedRam.name == ramOptions.name}
                          <option value={ramOption.name} selected>{ramOption.name} - €{ramOption.price}</option>
                        {:else}
                          <option value={ramOption.name}>{ramOption.name} - €{ramOption.price}</option>
                        {/if}
                        {/each}
                      </select>
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="div-63">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/8ba35bbbaf27638a4d9cf99e2bac5a2b01e4fcb4fbd10bd5a06e9508c9f712b8?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/8ba35bbbaf27638a4d9cf99e2bac5a2b01e4fcb4fbd10bd5a06e9508c9f712b8?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/8ba35bbbaf27638a4d9cf99e2bac5a2b01e4fcb4fbd10bd5a06e9508c9f712b8?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/8ba35bbbaf27638a4d9cf99e2bac5a2b01e4fcb4fbd10bd5a06e9508c9f712b8?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/8ba35bbbaf27638a4d9cf99e2bac5a2b01e4fcb4fbd10bd5a06e9508c9f712b8?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/8ba35bbbaf27638a4d9cf99e2bac5a2b01e4fcb4fbd10bd5a06e9508c9f712b8?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/8ba35bbbaf27638a4d9cf99e2bac5a2b01e4fcb4fbd10bd5a06e9508c9f712b8?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/8ba35bbbaf27638a4d9cf99e2bac5a2b01e4fcb4fbd10bd5a06e9508c9f712b8?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-21"
              />
              <div class="div-64">
                <div class="div-65">Scheda grafica</div>
                <div class="div-66">
                  <div class="div-67">
                    <label>
                      Scheda video:
                      <select bind:value={selectedGraphicsCard.name}>
                        {#each graphicsCards as graphicsCard}
                        {#if selectedGraphicsCard.name == graphicsCard.name}
                        <option value={graphicsCard.name} selected>{graphicsCard.name} - €{graphicsCard.price}</option>
                        {:else}
                          <option value={graphicsCard.name}>{graphicsCard.name} - €{graphicsCard.price}</option>
                        {/if}
                        {/each}
                      </select>
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="div-70">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/b0fbe5cfb0f79ffbaab24af51d99a1982c3187eaad76b726e47aaa1db6531401?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/b0fbe5cfb0f79ffbaab24af51d99a1982c3187eaad76b726e47aaa1db6531401?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/b0fbe5cfb0f79ffbaab24af51d99a1982c3187eaad76b726e47aaa1db6531401?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/b0fbe5cfb0f79ffbaab24af51d99a1982c3187eaad76b726e47aaa1db6531401?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/b0fbe5cfb0f79ffbaab24af51d99a1982c3187eaad76b726e47aaa1db6531401?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/b0fbe5cfb0f79ffbaab24af51d99a1982c3187eaad76b726e47aaa1db6531401?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/b0fbe5cfb0f79ffbaab24af51d99a1982c3187eaad76b726e47aaa1db6531401?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/b0fbe5cfb0f79ffbaab24af51d99a1982c3187eaad76b726e47aaa1db6531401?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-23"
              />
              <div class="div-71">
                <div class="div-72">Alimentatore</div>
                <div class="div-73">
                  <div class="div-74">
                    <label>
                      Alimentatore:
                      <select bind:value={selectedPowerSupply.name}>
                        {#each powerSupplies as powerSupply}
                        {#if selectedPowerSupply.name == powerSupply.name}
                          <option value={powerSupply.name} selected>{powerSupply.name} - €{powerSupply.price}</option>
                        {:else}
                          <option value={powerSupply.name} >{powerSupply.name} - €{powerSupply.price}</option>
                        {/if}
                        {/each}
                      </select>
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="div-77">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/57f828bba1217cf597a4e6792cb092f86de95dfa37be2a7d8bb5d227ea2c39e8?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/57f828bba1217cf597a4e6792cb092f86de95dfa37be2a7d8bb5d227ea2c39e8?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/57f828bba1217cf597a4e6792cb092f86de95dfa37be2a7d8bb5d227ea2c39e8?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/57f828bba1217cf597a4e6792cb092f86de95dfa37be2a7d8bb5d227ea2c39e8?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/57f828bba1217cf597a4e6792cb092f86de95dfa37be2a7d8bb5d227ea2c39e8?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/57f828bba1217cf597a4e6792cb092f86de95dfa37be2a7d8bb5d227ea2c39e8?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/57f828bba1217cf597a4e6792cb092f86de95dfa37be2a7d8bb5d227ea2c39e8?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/57f828bba1217cf597a4e6792cb092f86de95dfa37be2a7d8bb5d227ea2c39e8?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-25"
              />
              <div class="div-78">
                <div class="div-79">Schermo</div>
                <div class="div-80">
                  <div class="div-81">
                    <label>
                      Schermo:
                      <select bind:value={selectedScreen.name} on:change={() => calculateTotal(selectedProcessor, selectedMotherboard, selectedGraphicsCard, selectedPowerSupply, selectedRam, selectedStorage, selectedCase, selectedScreen)}>
                        {#each screens as screen}
                          {#if selectedScreen.name == screen.name}
                            <option value={screen.name} selected>{screen.name} - €{screen.price}</option>
                          {:else}
                            <option value={screen.name}>{screen.name} - €{screen.price}</option>
                          {/if}
                        {/each}
                      </select>
                    </label>                     
                  </div>
                </div>
              </div>
            </div>
            <div class="div-88">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/e9429030d8f5eb940d60020d7938ad7524b3cd4f09ed7dd6deb7074fe94d9797?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/e9429030d8f5eb940d60020d7938ad7524b3cd4f09ed7dd6deb7074fe94d9797?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/e9429030d8f5eb940d60020d7938ad7524b3cd4f09ed7dd6deb7074fe94d9797?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/e9429030d8f5eb940d60020d7938ad7524b3cd4f09ed7dd6deb7074fe94d9797?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/e9429030d8f5eb940d60020d7938ad7524b3cd4f09ed7dd6deb7074fe94d9797?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/e9429030d8f5eb940d60020d7938ad7524b3cd4f09ed7dd6deb7074fe94d9797?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/e9429030d8f5eb940d60020d7938ad7524b3cd4f09ed7dd6deb7074fe94d9797?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/e9429030d8f5eb940d60020d7938ad7524b3cd4f09ed7dd6deb7074fe94d9797?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-27"
              />
              <div class="div-89">
                <div class="div-90">Tastiera e mouse</div>
                <div class="div-91">
                  <div class="div-92">
                    <label>
                      Tastiera:
                      <select bind:value={selectedKeyboard.name} on:change={() => calculateTotal(selectedProcessor, selectedMotherboard, selectedGraphicsCard, selectedPowerSupply, selectedRam, selectedStorage, selectedCase, selectedScreen, selectedKeyboard, selectedMouse, selectedChair, selectedSpeakers, selectedMicrophone)}>
                        {#each keyboards as keyboard}
                          {#if selectedKeyboard.name == keyboard.name}
                            <option value={keyboard.name} selected>{keyboard.name} - €{keyboard.price}</option>
                          {:else}
                            <option value={keyboard.name}>{keyboard.name} - €{keyboard.price}</option>
                          {/if}
                        {/each}
                      </select>
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="div-95">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/dae2bc55ff55bcf5865bd9e1ade01be895f97fc36797ff1d614bceda59a37285?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/dae2bc55ff55bcf5865bd9e1ade01be895f97fc36797ff1d614bceda59a37285?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/dae2bc55ff55bcf5865bd9e1ade01be895f97fc36797ff1d614bceda59a37285?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/dae2bc55ff55bcf5865bd9e1ade01be895f97fc36797ff1d614bceda59a37285?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/dae2bc55ff55bcf5865bd9e1ade01be895f97fc36797ff1d614bceda59a37285?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/dae2bc55ff55bcf5865bd9e1ade01be895f97fc36797ff1d614bceda59a37285?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/dae2bc55ff55bcf5865bd9e1ade01be895f97fc36797ff1d614bceda59a37285?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/dae2bc55ff55bcf5865bd9e1ade01be895f97fc36797ff1d614bceda59a37285?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-29"
              />
              <div class="div-96">
                <div class="div-97">Mouse</div>
                <div class="div-98">
                  <div class="div-99">
                    <label>
                      Mouse:
                      <select bind:value={selectedMouse.name} on:change={() => calculateTotal(selectedProcessor, selectedMotherboard, selectedGraphicsCard, selectedPowerSupply, selectedRam, selectedStorage, selectedCase, selectedScreen, selectedKeyboard, selectedMouse, selectedChair, selectedSpeakers, selectedMicrophone)}>
                        {#each mice as mouse}
                          {#if selectedMouse.name == mouse.name}
                            <option value={mouse.name} selected>{mouse.name} - €{mouse.price}</option>
                          {:else}
                            <option value={mouse.name}>{mouse.name} - €{mouse.price}</option>
                          {/if}
                        {/each}
                      </select>
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="div-102">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/636ffc3729232ce5bfdc95476e4486d6f46293e939d69884422ea6d04ca80893?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/636ffc3729232ce5bfdc95476e4486d6f46293e939d69884422ea6d04ca80893?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/636ffc3729232ce5bfdc95476e4486d6f46293e939d69884422ea6d04ca80893?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/636ffc3729232ce5bfdc95476e4486d6f46293e939d69884422ea6d04ca80893?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/636ffc3729232ce5bfdc95476e4486d6f46293e939d69884422ea6d04ca80893?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/636ffc3729232ce5bfdc95476e4486d6f46293e939d69884422ea6d04ca80893?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/636ffc3729232ce5bfdc95476e4486d6f46293e939d69884422ea6d04ca80893?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/636ffc3729232ce5bfdc95476e4486d6f46293e939d69884422ea6d04ca80893?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-31"
              />
              <div class="div-103">
                <div class="div-104">Sedia da gaming</div>
                <div class="div-105">
                  <div class="div-106">
                    <label>
                      Sedia da Gaming:
                      <select bind:value={selectedChair.name} on:change={() => calculateTotal(selectedProcessor, selectedMotherboard, selectedGraphicsCard, selectedPowerSupply, selectedRam, selectedStorage, selectedCase, selectedScreen, selectedKeyboard, selectedMouse, selectedChair, selectedSpeakers, selectedMicrophone)}>
                        {#each gamingChairs as chair}
                          {#if selectedChair.name == chair.name}
                            <option value={chair.name} selected>{chair.name} - €{chair.price}</option>
                          {:else}
                            <option value={chair.name}>{chair.name} - €{chair.price}</option>
                          {/if}
                        {/each}
                      </select>
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="div-109">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/16cb486cdc464af4475c1598c7924f791085208831350c70e44ea5666679cf4a?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/16cb486cdc464af4475c1598c7924f791085208831350c70e44ea5666679cf4a?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/16cb486cdc464af4475c1598c7924f791085208831350c70e44ea5666679cf4a?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/16cb486cdc464af4475c1598c7924f791085208831350c70e44ea5666679cf4a?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/16cb486cdc464af4475c1598c7924f791085208831350c70e44ea5666679cf4a?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/16cb486cdc464af4475c1598c7924f791085208831350c70e44ea5666679cf4a?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/16cb486cdc464af4475c1598c7924f791085208831350c70e44ea5666679cf4a?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/16cb486cdc464af4475c1598c7924f791085208831350c70e44ea5666679cf4a?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-33"
              />
              <div class="div-110">
                <div class="div-111">Casse</div>
                <div class="div-112">
                  <div class="div-113">
                    <label>
                      Casse:
                      <select bind:value={selectedSpeakers.name} on:change={() => calculateTotal(selectedProcessor, selectedMotherboard, selectedGraphicsCard, selectedPowerSupply, selectedRam, selectedStorage, selectedCase, selectedScreen, selectedKeyboard, selectedMouse, selectedChair, selectedSpeakers, selectedMicrophone)}>
                        {#each speakerSystems as speakers}
                          {#if selectedSpeakers.name == speakers.name}
                            <option value={speakers.name} selected>{speakers.name} - €{speakers.price}</option>
                          {:else}
                            <option value={speakers.name}>{speakers.name} - €{speakers.price}</option>
                          {/if}
                        {/each}
                      </select>
                    </label>
                  </div>
                </div>
              </div>
            </div>
            <div class="div-116">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/bf61ff0521e3993de8224954ee09db789feb5c99fc3a777f979a928d98b8620f?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/bf61ff0521e3993de8224954ee09db789feb5c99fc3a777f979a928d98b8620f?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/bf61ff0521e3993de8224954ee09db789feb5c99fc3a777f979a928d98b8620f?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/bf61ff0521e3993de8224954ee09db789feb5c99fc3a777f979a928d98b8620f?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/bf61ff0521e3993de8224954ee09db789feb5c99fc3a777f979a928d98b8620f?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/bf61ff0521e3993de8224954ee09db789feb5c99fc3a777f979a928d98b8620f?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/bf61ff0521e3993de8224954ee09db789feb5c99fc3a777f979a928d98b8620f?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/bf61ff0521e3993de8224954ee09db789feb5c99fc3a777f979a928d98b8620f?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-35"
              />
              <div class="div-117">
                <div class="div-118">Microfono</div>
                <div class="div-119">
                  <div class="div-120">
                    <label>
                      Microfoni:
                      <select bind:value={selectedMicrophone.name} on:change={() => calculateTotal(selectedProcessor, selectedMotherboard, selectedGraphicsCard, selectedPowerSupply, selectedRam, selectedStorage, selectedCase, selectedScreen, selectedKeyboard, selectedMouse, selectedChair, selectedSpeakers, selectedMicrophone)}>
                        {#each microphones as microphone}
                          {#if selectedMicrophone.name == microphone.name}
                            <option value={microphone.name} selected>{microphone.name} - €{microphone.price}</option>
                          {:else}
                            <option value={microphone.name}>{microphone.name} - €{microphone.price}</option>
                          {/if}
                        {/each}
                      </select>
                    </label>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
    </div>
            </div>
          </div>
          <div class="div-74">&quot;</div>
        </div>
    </main>
    






















    <style>
        .div {
            display: flex;
            flex-direction: column;
          }
        div-2 {
            max-width: 100%;
            background-color: var(--www-pcspecialist-it-nero, #fff);
            display: flex;
            margin-top: 124px;
            width: 1170px;
            flex-direction: column;
            padding: 1px 0;
          }
          @media (max-width: 991px) {
            .div-2 {
              margin-top: 40px;
            }
          }
          .div-3 {
            background-color: var(--www-pcspecialist-it-mine-shaft, #3a3a3a);
            display: flex;
            padding-top: 21px;
            flex-direction: column;
          }
          @media (max-width: 991px) {
            .div-3 {
              max-width: 100%;
            }
          }
          .div-4 {
            color: var(--www-pcspecialist-it-nero, #fff);
            text-transform: uppercase;
            align-self: start;
            margin-left: 20px;
            white-space: nowrap;
            font: 600 18px/111% Montserrat, sans-serif;
          }
          @media (max-width: 991px) {
            .div-4 {
              margin-left: 10px;
              white-space: initial;
            }
          }
          .div-5 {
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            margin-top: 20px;
            flex-direction: column;
            justify-content: center;
            padding: 0 20px;
          }
          @media (max-width: 991px) {
            .div-5 {
              max-width: 100%;
            }
          }
          .div-6 {
            display: flex;
            width: 100%;
            justify-content: space-between;
            gap: 20px;
          }
          @media (max-width: 991px) {
            .div-6 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-7 {
            display: flex;
            justify-content: space-between;
            gap: 20px;
            padding: 8px 80px 8px 0;
          }
          @media (max-width: 991px) {
            .div-7 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-right: 20px;
            }
          }
          .div-8 {
            color: var(--www-pcspecialist-it-black, #000);
            text-align: center;
            text-transform: uppercase;
            flex-grow: 1;
            white-space: nowrap;
            margin: auto 0;
            font: 400 14px/100% Montserrat, sans-serif;
          }
          @media (max-width: 991px) {
            .div-8 {
              white-space: initial;
            }
          }
          .div-9 {
            color: var(--www-pcspecialist-it-jungle-green, #31b28b);
            text-align: center;
            white-space: nowrap;
            background-color: var(--www-pcspecialist-it-nero, #fff);
            flex-grow: 1;
            justify-content: center;
            padding: 15px 14px;
            font: 700 16px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-9 {
              white-space: initial;
            }
          }
          .div-10 {
            margin: auto 0;
            padding: 9px 53px 9px 11px;
            font: 400 14px/14px Montserrat, sans-serif;
          }
          @media (max-width: 991px) {
            .div-10 {
              padding-right: 20px;
            }
          }
          .div-11 {
            max-width: 1170px;
            background-color: var(--www-pcspecialist-it-nero, #fff);
            display: flex;
            flex-direction: column;
            padding: 20px 20px 0;
          }
          @media (max-width: 991px) {
            .div-11 {
              max-width: 100%;
            }
          }
          .div-12 {
            background-color: var(--www-pcspecialist-it-nero, #fff);
            display: flex;
            flex-direction: column;
          }
          @media (max-width: 991px) {
            .div-12 {
              max-width: 100%;
            }
          }
          .div-13 {
            color: var(--www-pcspecialist-it-nero, #fff);
            text-transform: uppercase;
            white-space: nowrap;
            align-items: start;
            background-color: var(--www-pcspecialist-it-black, #000);
            justify-content: center;
            padding: 15px 60px 15px 20px;
            font: 400 14px/150% Montserrat, sans-serif;
          }
          @media (max-width: 991px) {
            .div-13 {
              white-space: initial;
              max-width: 100%;
              padding-right: 20px;
            }
          }
          .div-14 {
            max-width: 1130px;
            border-right: 1px solid var(--www-pcspecialist-it-alto, #ddd);
            border-bottom: 1px solid var(--www-pcspecialist-it-alto, #ddd);
            border-left: 1px solid var(--www-pcspecialist-it-alto, #ddd);
            display: flex;
            flex-direction: column;
            padding: 0 1px 9px;
          }
          @media (max-width: 991px) {
            .div-14 {
              max-width: 100%;
            }
          } 
          .div-41 {
            color: var(--www-pcspecialist-it-nero, #fff);
            text-transform: uppercase;
            white-space: nowrap;
            justify-content: center;
            align-items: start;
            background-color: var(--www-pcspecialist-it-black, #000);
            margin-top: 25px;
            padding: 15px 60px 15px 20px;
            font: 400 14px/150% Montserrat, sans-serif;
          }
          @media (max-width: 991px) {
            .div-41 {
              white-space: initial;
              max-width: 100%;
              padding-right: 20px;
            }
          }
          .div-42 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 14px 10px 14px 21px;
          }
          @media (max-width: 991px) {
            .div-42 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-15 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-43 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-43 {
              max-width: 100%;
            }
          }
          .div-44 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-44 {
              max-width: 100%;
            }
          }
          .div-45 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-45 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-46 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
          }
          @media (max-width: 991px) {
            .div-46 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-49 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 14px 10px 14px 21px;
          }
          @media (max-width: 991px) {
            .div-49 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-17 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-50 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-50 {
              max-width: 100%;
            }
          }
          .div-51 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-51 {
              max-width: 100%;
            }
          }
          .div-52 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-52 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-53 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
          }
          @media (max-width: 991px) {
            .div-53 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-56 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 14px 10px 14px 21px;
          }
          @media (max-width: 991px) {
            .div-56 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-19 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-57 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-57 {
              max-width: 100%;
            }
          }
          .div-58 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-58 {
              max-width: 100%;
            }
          }
          .div-59 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-59 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-60 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
          }
          @media (max-width: 991px) {
            .div-60 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-63 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 14px 10px 14px 21px;
          }
          @media (max-width: 991px) {
            .div-63 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-21 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-64 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-64 {
              max-width: 100%;
            }
          }
          .div-65 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-65 {
              max-width: 100%;
            }
          }
          .div-66 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-66 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-67 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
          }
          @media (max-width: 991px) {
            .div-67 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-70 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 9px 10px 9px 21px;
          }
          @media (max-width: 991px) {
            .div-70 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-23 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            align-self: start;
            margin-top: 18px;
          }
          .div-71 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-71 {
              max-width: 100%;
            }
          }
          .div-72 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-72 {
              max-width: 100%;
            }
          }
          .div-73 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-73 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-74 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
          }
          @media (max-width: 991px) {
            .div-74 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-77 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 14px 10px 14px 21px;
          }
          @media (max-width: 991px) {
            .div-77 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-25 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-78 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-78 {
              max-width: 100%;
            }
          }
          .div-79 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-79 {
              max-width: 100%;
            }
          }
          .div-80 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 0px;
          }
          @media (max-width: 991px) {
            .div-80 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-81 {
            display: flex;
            justify-content: space-between;
            gap: 20px;
          }
          @media (max-width: 991px) {
            .div-81 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-88 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 14px 10px 14px 21px;
          }
          @media (max-width: 991px) {
            .div-88 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-27 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-89 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-89 {
              max-width: 100%;
            }
          }
          .div-90 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-90 {
              max-width: 100%;
            }
          }
          .div-91 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-91 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-92 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
          }
          @media (max-width: 991px) {
            .div-92 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-95 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 14px 10px 14px 21px;
          }
          @media (max-width: 991px) {
            .div-95 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-29 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-96 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-96 {
              max-width: 100%;
            }
          }
          .div-97 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-97 {
              max-width: 100%;
            }
          }
          .div-98 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-98 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-99 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
          }
          @media (max-width: 991px) {
            .div-99 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-102 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 14px 10px 14px 21px;
          }
          @media (max-width: 991px) {
            .div-102 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-31 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-103 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-103 {
              max-width: 100%;
            }
          }
          .div-104 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-104 {
              max-width: 100%;
            }
          }
          .div-105 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-105 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-106 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
          }
          @media (max-width: 991px) {
            .div-106 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-109 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 14px 10px 14px 21px;
          }
          @media (max-width: 991px) {
            .div-109 {
              max-width: 100%;
              flex-wrap: wrap;
              padding-left: 20px;
            }
          }
          .img-33 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-110 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 10px 0;
          }
          @media (max-width: 991px) {
            .div-110 {
              max-width: 100%;
            }
          }
          .div-111 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-111 {
              max-width: 100%;
            }
          }
          .div-112 {
            display: flex;
            margin-top: 10px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-112 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-113 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
          }
          @media (max-width: 991px) {
            .div-113 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-116 {
            justify-content: space-between;
            background-color: var(--www-pcspecialist-it-gallery, #ebebeb);
            display: flex;
            gap: 20px;
            padding: 13px 10px 13px 20px;
          }
          @media (max-width: 991px) {
            .div-116 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .img-35 {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 60px;
            margin: auto 0;
          }
          .div-117 {
            display: flex;
            flex-grow: 1;
            flex-basis: 0%;
            flex-direction: column;
            padding: 0 7px 11px 0;
          }
          @media (max-width: 991px) {
            .div-117 {
              max-width: 100%;
            }
          }
          .div-118 {
            color: var(--www-pcspecialist-it-lochinvar, #2d8f71);
            font: 700 14px/150% Open Sans, sans-serif;
          }
          @media (max-width: 991px) {
            .div-118 {
              max-width: 100%;
            }
          }
          .div-119 {
            display: flex;
            margin-top: 7px;
            justify-content: space-between;
            gap: 18px;
          }
          @media (max-width: 991px) {
            .div-119 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-120 {
            display: flex;
            justify-content: space-between;
            gap: 4px;
            padding: 1px 0;
          }
          @media (max-width: 991px) {
            .div-120 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-123 {
            justify-content: center;
            align-items: center;
            border-bottom: 2.4px solid
              var(
                --12700155001519199951171875-x-6775999755859375-default-purple,
                #64ffce
              );
            background-color: var(
              --12700155001519199951171875-x-6775999755859375-default-black,
              #000
            );
            display: flex;
            width: 100%;
            flex-direction: column;
            padding: 1px 60px;
            position: fixed;
            top: 0;
            left: 0;
            z-index: 1000; /* Imposta un valore di z-index per sovrapporre l'elemento a eventuali altri elementi sulla pagina */
            background-color: #000; /* Imposta il colore di sfondo desiderato */
            /* Aggiungi eventuali altri stili desiderati */
          }
          @media (max-width: 991px) {
            .div-123 {
              max-width: 100%;
              padding: 0 20px;
            }
          }
          .div-124 {
            max-width: 1170px;
            justify-content: space-between;
            align-items: center;
            display: flex;
            width: 100%;
            gap: 20px;
          }
          @media (max-width: 991px) {
            .div-124 {
              max-width: 100%;
              flex-wrap: wrap;
            }
          }
          .div-125 {
            text-align: center;
            -webkit-text-stroke-width: 1;
            -webkit-text-stroke-color: var(
              --12700155001519199951171875-x-6775999755859375-default-nero-60,
              rgba(255, 255, 255, 0.6)
            );
            letter-spacing: 3px;
            text-decoration-line: underline;
            text-transform: uppercase;
            align-self: stretch;
            justify-content: center;
            margin: auto 0;
            padding: 0 1px;
            font: 400 32px/115% Arial, sans-serif;
          }
          .img {
            aspect-ratio: 1;
            object-fit: contain;
            object-position: center;
            width: 70px;
            align-self: stretch;
            margin: auto 0;
          }
          .div-126 {
            align-self: stretch;
            display: flex;
            justify-content: space-between;
            gap: 20px;
            font-size: 13px;
            color: var(
              --12700155001519199951171875-x-6775999755859375-default-nero,
              #fff
            );
            font-weight: 400;
            text-transform: uppercase;
            padding: 30px 15px;
          }
          .div-127 {
            font-family: Montserrat, sans-serif;
            line-height: 150%;
          }
          .div-128 {
            font-family: Montserrat, sans-serif;
            line-height: 150%;
          }
          .div-129 {
            justify-content: center;
            background-color: var(
              --12700155001519199951171875-x-6775999755859375-default-silver,
              #cbcbcb
            );
            display: flex;
            width: 100%;
            flex-direction: column;
          }
          @media (max-width: 991px) {
            .div-129 {
              max-width: 100%;
            }
          }
          .div-130 {
            disply: flex;
            flex-direction: column;
            overflow: hidden;
            position: relative;
            display: flex;
            min-height: 1381px;
            width: 100%;
            justify-content: center;
            align-items: center;
            padding: 30px 60px;
          }
          @media (max-width: 991px) {
            .div-130 {
              max-width: 100%;
              padding: 0 20px;
            }
          }
               /*bottone iniziale iis castelli*/
            /* === removing default button style ===*/
          .button {
            margin: 0;
            height: auto;
            background: transparent;
            padding: 0;
            border: none;
            cursor: pointer;
          }
          
          /* button styling */
          .button {
            --border-right: 6px;
            --text-stroke-color: rgba(255,255,255,0.6);
            --animation-color: #37FF8B;
            --fs-size: 2em;
            letter-spacing: 3px;
            text-decoration: none;
            font-size: var(--fs-size);
            font-family: "Arial";
            position: relative;
            text-transform: uppercase;
            color: transparent;
            -webkit-text-stroke: 1px var(--text-stroke-color);
          }
          /* this is the text, when you hover on button */
          .hover-text {
            position: absolute;
            box-sizing: border-box;
            content: attr(data-text);
            color: var(--animation-color);
            width: 0%;
            inset: 0;
            border-right: var(--border-right) solid var(--animation-color);
            overflow: hidden;
            transition: 0.5s;
            -webkit-text-stroke: 1px var(--animation-color);
          }
          /* hover */
          .button:hover .hover-text {
            width: 100%;
            filter: drop-shadow(0 0 23px var(--animation-color))
          }
          
          
          /*bottoni recensioni e chi siamo*/
          .btn {
            outline: 0;
            display: inline-flex;
            align-items: center;
            justify-content: space-between;
            background: #40B3A2;
            min-width: 200px;
            border: 0;
            border-radius: 4px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, .1);
            box-sizing: border-box;
            padding: 16px 20px;
            color: #fff;
            font-size: 12px;
            font-weight: 600;
            letter-spacing: 1.2px;
            text-transform: uppercase;
            overflow: hidden;
            cursor: pointer;
          }
          
          .btn:hover {
            opacity: .95;
          }
          
          .btn .animation {
            border-radius: 100%;
            animation: ripple 0.6s linear infinite;
          }
          
          @keyframes ripple {
            0% {
              box-shadow: 0 0 0 0 rgba(255, 255, 255, 0.1), 0 0 0 20px rgba(255, 255, 255, 0.1), 0 0 0 40px rgba(255, 255, 255, 0.1), 0 0 0 60px rgba(255, 255, 255, 0.1);
            }
          
            100% {
              box-shadow: 0 0 0 20px rgba(255, 255, 255, 0.1), 0 0 0 40px rgba(255, 255, 255, 0.1), 0 0 0 60px rgba(255, 255, 255, 0.1), 0 0 0 80px rgba(255, 255, 255, 0);
            }
          }
          
          /*loader*/
          .loader {
            width: 48px;
            height: 48px;
            margin: auto;
            position: relative;
          }
          
          .loader:before {
            content: '';
            width: 48px;
            height: 5px;
            background: #f0808050;
            position: absolute;
            top: 60px;
            left: 0;
            border-radius: 50%;
            animation: shadow324 0.5s linear infinite;
          }
          
          .loader:after {
            content: '';
            width: 100%;
            height: 100%;
            background: #f08080;
            position: absolute;
            top: 0;
            left: 0;
            border-radius: 4px;
            animation: jump7456 0.5s linear infinite;
          }
          
          @keyframes jump7456 {
            15% {
              border-bottom-right-radius: 3px;
            }
          
            25% {
              transform: translateY(9px) rotate(22.5deg);
            }
          
            50% {
              transform: translateY(18px) scale(1, .9) rotate(45deg);
              border-bottom-right-radius: 40px;
            }
          
            75% {
              transform: translateY(9px) rotate(67.5deg);
            }
          
            100% {
              transform: translateY(0) rotate(90deg);
            }
          }
          
          @keyframes shadow324 {
          
          0%,
            100% {
            transform: scale(1, 1);
          }
        
          50% {
            transform: scale(1.2, 1);
          }
        }
        



                /*BOTTONE PROSEGUI*/
          .cssbuttons-io-button {
          background: #a370f0;
          color: white;
          font-family: inherit;
          padding: 0.35em;
          padding-left: 1.2em;
          font-size: 17px;
          font-weight: 500;
          border-radius: 0.9em;
          border: none;
          letter-spacing: 0.05em;
          display: flex;
          align-items: center;
          box-shadow: inset 0 0 1.6em -0.6em #714da6;
          overflow: hidden;
          position: relative;
          height: 2.8em;
          padding-right: 3.3em;
          cursor: pointer;
        }

        .cssbuttons-io-button .icon {
          background: white;
          margin-left: 1em;
          position: absolute;
          display: flex;
          align-items: center;
          justify-content: center;
          height: 2.2em;
          width: 2.2em;
          border-radius: 0.7em;
          box-shadow: 0.1em 0.1em 0.6em 0.2em #7b52b9;
          right: 0.3em;
          transition: all 0.3s;
        }

        .cssbuttons-io-button:hover .icon {
          width: calc(100% - 0.6em);
        }

        .cssbuttons-io-button .icon svg {
          width: 1.1em;
          transition: transform 0.3s;
          color: #7b52b9;
        }

        .cssbuttons-io-button:hover .icon svg {
          transform: translateX(0.1em);
        }

        .cssbuttons-io-button:active .icon {
          transform: scale(0.95);
        }

        


        /*OVERLAPPING*/
        @import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap");
        *,
        *:before,
        *:after {
          box-sizing: border-box;
        }

        *,
        body,
        html {
          &::-webkit-scrollbar {
            background-color: #1e1f26;
            height: 20px;
            width: 20px;
          }

          &::-webkit-scrollbar-thumb {
            background: #383d4d;
            border-radius: 99em;
            border: 6px solid #1e1f26;
          }
        }

        html,
        body {
          margin: 0;
          padding: 0;
        }

        h1 {
          font-size: clamp(20px, 2.5vw, 36px);
          color: rgba(#fff, 0.8);
          font-weight: 600;
          text-align: center;
        }

        img {
          display: block;
          width: 100%;
          max-width: 100%;
          margin-bottom: 1.5rem;
        }

        ul {
          padding: 0;
          margin: 0;
          display: block;
          width: 100%;
          overflow-y: hidden;
          overflow-x: auto;
          white-space: nowrap;
          text-align: center;
          scroll-behavior: smooth;
        }

        li {
          position: -webkit-sticky;
          position: sticky;
          left: 0;
          width: min(50vw, 350px);
          display: inline-block;
          text-align: center;
          background-color: #16171f;
          color: #9b9dad;
          padding-bottom: 1.5rem;
          font-size: clamp(18px, 2.5vw, 22px);
          box-shadow: -10px 0 30px 0 rgba(#000, 0.25);
          margin-left: -4px;
        }

        body {
          font-family: "Inter", sans-serif;
          background-color: #1e1f26;
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          min-height: 100vh;
        }

    
        
       
    
    </style>