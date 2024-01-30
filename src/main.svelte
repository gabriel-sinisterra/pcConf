<script>
  import { navigate } from "svelte-routing";
  
  function goToReviewsPage() {
    navigate("/reviews");
  }

  function goToIntelPage() {
    navigate("/intel");
  }

  function goToAmdPage() {
    navigate("/amd");
  }
</script>
  
  <main>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <div class="div">
      <div class="div-2">
        <div class="div-3">
          <div class="div-4">
            <a href="/">
              <button class="button" data-text="Awesome">
                <span class="actual-text">&nbsp;IIS Castelli&nbsp;</span>
                <span aria-hidden="true" class="hover-text">&nbsp;IIS Castelli&nbsp;</span>
                <!-- svelte-ignore a11y-missing-content -->
              </button>
            </a>
          </div>
          <div class="loader"></div>
          <div class="div-5">
            <div class="div-6">
              <div>
                <a href="https://www.iiscastelli.edu.it/Pager.aspx?Page=mainpage"><button class="btn"><i class="animation"></i>Chi Siamo<i class="animation"></i></button>
                </a>
                
              </div>
            </div>
            <div class="div-7">
              <div>
                  <button class="btn" on:click={goToReviewsPage}><i class="animation"></i>Recensioni<i class="animation"></i>
                  </button>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="div-8">
        <div class="div-9">
          <!-- svelte-ignore a11y-missing-attribute -->
          <img
            loading="lazy"
            srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/1dabb93d87fa5ce6ba7372316664604627997592e09bdb71ca9b25a6d73a2dee?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/1dabb93d87fa5ce6ba7372316664604627997592e09bdb71ca9b25a6d73a2dee?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/1dabb93d87fa5ce6ba7372316664604627997592e09bdb71ca9b25a6d73a2dee?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/1dabb93d87fa5ce6ba7372316664604627997592e09bdb71ca9b25a6d73a2dee?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/1dabb93d87fa5ce6ba7372316664604627997592e09bdb71ca9b25a6d73a2dee?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/1dabb93d87fa5ce6ba7372316664604627997592e09bdb71ca9b25a6d73a2dee?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/1dabb93d87fa5ce6ba7372316664604627997592e09bdb71ca9b25a6d73a2dee?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/1dabb93d87fa5ce6ba7372316664604627997592e09bdb71ca9b25a6d73a2dee?apiKey=2063adc69d1343799b861ebfdc37587c&"
            class="img-2"
          />
          <div class="div-10">
            <div class="div-11">
              <!-- svelte-ignore a11y-missing-attribute -->
              <img
                loading="lazy"
                srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/7be006aaf66e007a105a5ef829424007086938c93034f2bc16cb14f5c98e01a3?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/7be006aaf66e007a105a5ef829424007086938c93034f2bc16cb14f5c98e01a3?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/7be006aaf66e007a105a5ef829424007086938c93034f2bc16cb14f5c98e01a3?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/7be006aaf66e007a105a5ef829424007086938c93034f2bc16cb14f5c98e01a3?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/7be006aaf66e007a105a5ef829424007086938c93034f2bc16cb14f5c98e01a3?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/7be006aaf66e007a105a5ef829424007086938c93034f2bc16cb14f5c98e01a3?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/7be006aaf66e007a105a5ef829424007086938c93034f2bc16cb14f5c98e01a3?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/7be006aaf66e007a105a5ef829424007086938c93034f2bc16cb14f5c98e01a3?apiKey=2063adc69d1343799b861ebfdc37587c&"
                class="img-3"
              />
              <div class="div-12">Costruisci Il Tuo PC</div>
            </div>
            <div class="div-13">
              <div class="div-14">
                <div class="column">
                  <div class="div-15">
                    <div class="div-16">
                      <!-- svelte-ignore a11y-missing-attribute -->
                      <img
                        loading="lazy"
                        srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/07bec44ff310294ed05c58d3d377e905bb0048775eb03a26e485158c0bf5b987?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/07bec44ff310294ed05c58d3d377e905bb0048775eb03a26e485158c0bf5b987?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/07bec44ff310294ed05c58d3d377e905bb0048775eb03a26e485158c0bf5b987?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/07bec44ff310294ed05c58d3d377e905bb0048775eb03a26e485158c0bf5b987?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/07bec44ff310294ed05c58d3d377e905bb0048775eb03a26e485158c0bf5b987?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/07bec44ff310294ed05c58d3d377e905bb0048775eb03a26e485158c0bf5b987?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/07bec44ff310294ed05c58d3d377e905bb0048775eb03a26e485158c0bf5b987?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/07bec44ff310294ed05c58d3d377e905bb0048775eb03a26e485158c0bf5b987?apiKey=2063adc69d1343799b861ebfdc37587c&"
                        class="img-4"
                      />
                    </div>
                    <div class="div-17">Intel Costruisci Il Tuo PC</div>
                    <div class="div-18">
                      Lavora, gioca e crea rapidamente e senza
                      <br />
                      intoppi.
                    </div>
                    <!-- svelte-ignore a11y-missing-attribute -->
                    <img
                      loading="lazy"
                      srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/85efff4963fe85ad93fbbdea8371d2fcb3a5d219930de0e43ccb90ac18a73ccb?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/85efff4963fe85ad93fbbdea8371d2fcb3a5d219930de0e43ccb90ac18a73ccb?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/85efff4963fe85ad93fbbdea8371d2fcb3a5d219930de0e43ccb90ac18a73ccb?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/85efff4963fe85ad93fbbdea8371d2fcb3a5d219930de0e43ccb90ac18a73ccb?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/85efff4963fe85ad93fbbdea8371d2fcb3a5d219930de0e43ccb90ac18a73ccb?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/85efff4963fe85ad93fbbdea8371d2fcb3a5d219930de0e43ccb90ac18a73ccb?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/85efff4963fe85ad93fbbdea8371d2fcb3a5d219930de0e43ccb90ac18a73ccb?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/85efff4963fe85ad93fbbdea8371d2fcb3a5d219930de0e43ccb90ac18a73ccb?apiKey=2063adc69d1343799b861ebfdc37587c&"
                      class="img-5"
                    />
                    <div class="div-19">
                      Scegli fra Intel® Core™ i3, i5, i7, i9, Intel® Xeon®,
                      <br />
                      Intel® Celeron® & Intel® Pentium® Processore.
                    </div>
                      <div class="div-20">
                        <button class="learn-more" on:click={goToIntelPage}>
                          <span class="circle" aria-hidden="true">
                          <span class="icon arrow"></span>
                          </span>
                          <span class="button-text">Configura PC</span>
                        </button>
                      </div>
                    </div>
                </div>
                <div class="column-2">
                  <div class="div-21">
                    <div class="div-22">
                      <!-- svelte-ignore a11y-missing-attribute -->
                      <img
                        loading="lazy"
                        srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/3b0f3390a7a28c9fab7d573738e4ca1a38bca9593e5924f54cf384efba2e2ca2?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/3b0f3390a7a28c9fab7d573738e4ca1a38bca9593e5924f54cf384efba2e2ca2?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/3b0f3390a7a28c9fab7d573738e4ca1a38bca9593e5924f54cf384efba2e2ca2?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/3b0f3390a7a28c9fab7d573738e4ca1a38bca9593e5924f54cf384efba2e2ca2?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/3b0f3390a7a28c9fab7d573738e4ca1a38bca9593e5924f54cf384efba2e2ca2?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/3b0f3390a7a28c9fab7d573738e4ca1a38bca9593e5924f54cf384efba2e2ca2?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/3b0f3390a7a28c9fab7d573738e4ca1a38bca9593e5924f54cf384efba2e2ca2?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/3b0f3390a7a28c9fab7d573738e4ca1a38bca9593e5924f54cf384efba2e2ca2?apiKey=2063adc69d1343799b861ebfdc37587c&"
                        class="img-6"
                      />
                    </div>
                    <div class="div-23">AMD Costruisci Il Tuo PC</div>
                    <div class="div-24">prestazioni rapide e fluide con AMD</div>
                    <!-- svelte-ignore a11y-missing-attribute -->
                    <img
                      loading="lazy"
                      srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/d9e3d98c193218f630cb89e6631db1d0daef8370d99b66d4b4c2a90aae77e35b?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/d9e3d98c193218f630cb89e6631db1d0daef8370d99b66d4b4c2a90aae77e35b?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/d9e3d98c193218f630cb89e6631db1d0daef8370d99b66d4b4c2a90aae77e35b?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/d9e3d98c193218f630cb89e6631db1d0daef8370d99b66d4b4c2a90aae77e35b?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/d9e3d98c193218f630cb89e6631db1d0daef8370d99b66d4b4c2a90aae77e35b?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/d9e3d98c193218f630cb89e6631db1d0daef8370d99b66d4b4c2a90aae77e35b?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/d9e3d98c193218f630cb89e6631db1d0daef8370d99b66d4b4c2a90aae77e35b?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/d9e3d98c193218f630cb89e6631db1d0daef8370d99b66d4b4c2a90aae77e35b?apiKey=2063adc69d1343799b861ebfdc37587c&"
                      class="img-7"
                    />
                    <div class="div-25">
                      Scegli fra AMD Ryzen™, Threadripper™ e CPU con
                      <br />
                      tecnologia Athlon™.
                    </div>
                    <div class="div-26">
                      <button class="learn-more" on:click={goToAmdPage}>
                        <span class="circle" aria-hidden="true">
                        <span class="icon arrow"></span>
                        </span>
                        <span class="button-text">Configura PC</span>
                      </button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="div-27">
              <div class="div-28">
                <div class="column-3">
                  <div class="div-29">
                    <div class="div-30">Aurora Ultra</div>
                    <div class="div-31">
                      <!-- svelte-ignore a11y-missing-attribute -->
                      <img
                        loading="lazy"
                        srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/c2d87ce19ed86a0296fc2bd532cd9502efa2b95681503cb22bdc58da85a67c18?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/c2d87ce19ed86a0296fc2bd532cd9502efa2b95681503cb22bdc58da85a67c18?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/c2d87ce19ed86a0296fc2bd532cd9502efa2b95681503cb22bdc58da85a67c18?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/c2d87ce19ed86a0296fc2bd532cd9502efa2b95681503cb22bdc58da85a67c18?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/c2d87ce19ed86a0296fc2bd532cd9502efa2b95681503cb22bdc58da85a67c18?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/c2d87ce19ed86a0296fc2bd532cd9502efa2b95681503cb22bdc58da85a67c18?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/c2d87ce19ed86a0296fc2bd532cd9502efa2b95681503cb22bdc58da85a67c18?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/c2d87ce19ed86a0296fc2bd532cd9502efa2b95681503cb22bdc58da85a67c18?apiKey=2063adc69d1343799b861ebfdc37587c&"
                        class="img-8"
                      />
                      <div class="div-32">
                        <div class="div-33">Da</div>
                        <div class="div-34">€970</div>
                        <div class="div-35">incl. IVA e consegna.</div>
                      </div>
                      <div class="div-36">
                        <div class="div-37">Intel® Core™ i5-13500</div>
                        <div class="div-38">Windows 11 Home</div>
                        <div class="div-39">PCS PRO 3200 MHz 8 GB</div>
                        <div class="div-40">GEFORCE GT 1030 2 GB - DVI, HDMI</div>
                        <div class="div-41">SEAGATE BARRACUDA HDD 1 TB</div>
                        <div class="div-42">SOLIDIGM P41+ GEN 4 M.2 512 GB</div>
                      </div>
                      <div class="div-43">
                        <button id="bottone1"><strong>
                          Vai alla pagina
                        </strong></button>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="column-4">
                  <div class="div-44">
                    <div class="div-45">Zircon Nova</div>
                    <div class="div-46">
                      <!-- svelte-ignore a11y-missing-attribute -->
                      <img
                        loading="lazy"
                        srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/53f8c0ae2be9f9bae6ec71f86097f6fb7d7c170d0a229ed4c80daa588a946497?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/53f8c0ae2be9f9bae6ec71f86097f6fb7d7c170d0a229ed4c80daa588a946497?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/53f8c0ae2be9f9bae6ec71f86097f6fb7d7c170d0a229ed4c80daa588a946497?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/53f8c0ae2be9f9bae6ec71f86097f6fb7d7c170d0a229ed4c80daa588a946497?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/53f8c0ae2be9f9bae6ec71f86097f6fb7d7c170d0a229ed4c80daa588a946497?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/53f8c0ae2be9f9bae6ec71f86097f6fb7d7c170d0a229ed4c80daa588a946497?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/53f8c0ae2be9f9bae6ec71f86097f6fb7d7c170d0a229ed4c80daa588a946497?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/53f8c0ae2be9f9bae6ec71f86097f6fb7d7c170d0a229ed4c80daa588a946497?apiKey=2063adc69d1343799b861ebfdc37587c&"
                        class="img-9"
                      />
                      <div class="div-47">
                        <div class="div-48">Da</div>
                        <div class="div-49">€1.400</div>
                        <div class="div-50">incl. IVA e consegna</div>
                      </div>
                      <div class="div-51">
                        <div class="div-52">AMD Ryzen 5 7600</div>
                        <div class="div-53">Windows 11 Home</div>
                        <div class="div-54">Corsair VENGEANCE 4800 MHz 32 GB</div>
                        <div class="div-55">AMD RADEON™ RX 7600 8 GB</div>
                        <div class="div-56">SOLIDIGM P44 PRO GEN 4 M.2 512 GB</div>
                        <div class="div-57">ASUS® TUF GAMING X670E-PLUS WIFI</div>
                      </div>
                      <button id="bottone1"><strong>
                        Vai alla pagina
                      </strong></button>
                    </div>
                  </div>
                </div>
                <div class="column-5">
                  <div class="div-59">
                    <div class="div-60">Aero Supreme</div>
                    <div class="div-61">
                      <!-- svelte-ignore a11y-missing-attribute -->
                      <img
                        loading="lazy"
                        srcset="https://cdn.builder.io/api/v1/image/assets/TEMP/d588466bd11372b074ca09efae0b78a483506a86e35937818e5ab7ea27003c03?apiKey=2063adc69d1343799b861ebfdc37587c&width=100 100w, https://cdn.builder.io/api/v1/image/assets/TEMP/d588466bd11372b074ca09efae0b78a483506a86e35937818e5ab7ea27003c03?apiKey=2063adc69d1343799b861ebfdc37587c&width=200 200w, https://cdn.builder.io/api/v1/image/assets/TEMP/d588466bd11372b074ca09efae0b78a483506a86e35937818e5ab7ea27003c03?apiKey=2063adc69d1343799b861ebfdc37587c&width=400 400w, https://cdn.builder.io/api/v1/image/assets/TEMP/d588466bd11372b074ca09efae0b78a483506a86e35937818e5ab7ea27003c03?apiKey=2063adc69d1343799b861ebfdc37587c&width=800 800w, https://cdn.builder.io/api/v1/image/assets/TEMP/d588466bd11372b074ca09efae0b78a483506a86e35937818e5ab7ea27003c03?apiKey=2063adc69d1343799b861ebfdc37587c&width=1200 1200w, https://cdn.builder.io/api/v1/image/assets/TEMP/d588466bd11372b074ca09efae0b78a483506a86e35937818e5ab7ea27003c03?apiKey=2063adc69d1343799b861ebfdc37587c&width=1600 1600w, https://cdn.builder.io/api/v1/image/assets/TEMP/d588466bd11372b074ca09efae0b78a483506a86e35937818e5ab7ea27003c03?apiKey=2063adc69d1343799b861ebfdc37587c&width=2000 2000w, https://cdn.builder.io/api/v1/image/assets/TEMP/d588466bd11372b074ca09efae0b78a483506a86e35937818e5ab7ea27003c03?apiKey=2063adc69d1343799b861ebfdc37587c&"
                        class="img-10"
                      />
                      <div class="div-62">
                        <div class="div-63">Da</div>
                        <div class="div-64">€1.620</div>
                        <div class="div-65">incl. IVA e consegna.</div>
                      </div>
                      <div class="div-66">
                        <div class="div-67">AMD Ryzen 5 5600</div>
                        <div class="div-68">Windows 11 Home</div>
                        <div class="div-69">Corsair VENGEANCE 3200 MHz 16 GB</div>
                        <div class="div-70">
                          12 GB AMD RADEON™ RX 7700 XT GAMING
                        </div>
                        <div class="div-71">SSD KINGSTON A400 240 GB</div>
                        <div class="div-72">SEAGATE BARRACUDA HDD 2 TB</div>
                      </div>
                      <button id="bottone1"><strong>
                        Vai alla pagina
                      </strong></button>
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
      .div-2 {
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
        .div-2 {
          max-width: 100%;
          padding: 0 20px;
        }
      }
      .div-3 {
        max-width: 1170px;
        justify-content: space-between;
        align-items: center;
        display: flex;
        width: 100%;
        gap: 20px;
      }
      @media (max-width: 991px) {
        .div-3 {
          max-width: 100%;
          flex-wrap: wrap;
        }
      }
      .div-4 {
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
      .div-5 {
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
      .div-6 {
        font-family: Montserrat, sans-serif;
        line-height: 150%;
      }
      .div-7 {
        font-family: Montserrat, sans-serif;
        line-height: 150%;
      }
      .div-8 {
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
        .div-8 {
          max-width: 100%;
        }
      }
      .div-9 {
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
        .div-9 {
          max-width: 100%;
          padding: 0 20px;
        }
      }
      .img-2 {
        position: absolute;
        inset: 0;
        height: 100%;
        width: 100%;
        object-fit: cover;
        object-position: center;
      }
      .div-10 {
        position: relative;
        max-width: 1170px;
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        display: flex;
        width: 100%;
        flex-direction: column;
      }
      @media (max-width: 991px) {
        .div-10 {
          max-width: 100%;
        }
      }
      .div-11 {
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mine-shaft,
          #272727
        );
        display: flex;
        justify-content: space-between;
        gap: 0px;
      }
      @media (max-width: 991px) {
        .div-11 {
          max-width: 100%;
          flex-wrap: wrap;
        }
      }
      .img-3 {
        aspect-ratio: 1.11;
        object-fit: contain;
        object-position: center;
        width: 100px;
        max-width: 100%;
      }
      .div-12 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        text-transform: uppercase;
        flex-grow: 1;
        flex-basis: auto;
        margin: auto 0;
        font: 400 21px/129% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-12 {
          max-width: 100%;
        }
      }
      .div-13 {
        margin: 30px 30px 0;
      }
      @media (max-width: 991px) {
        .div-13 {
          max-width: 100%;
          margin-right: 10px;
        }
      }
      .div-14 {
        gap: 20px;
        display: flex;
      }
      @media (max-width: 991px) {
        .div-14 {
          flex-direction: column;
          align-items: stretch;
          gap: 0px;
        }
      }
      .column {
        display: flex;
        flex-direction: column;
        line-height: normal;
        width: 50%;
        margin-left: 0px;
      }
      @media (max-width: 991px) {
        .column {
          width: 100%;
        }
      }
      .div-15 {
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-gallery,
          #ebebeb
        );
        display: flex;
        flex-grow: 1;
        flex-direction: column;
        padding: 0 30px 30px;
      }
      @media (max-width: 991px) {
        .div-15 {
          max-width: 100%;
          margin-top: 20px;
          padding: 0 20px;
        }
      }
      .div-16 {
        justify-content: center;
        align-items: center;
        display: flex;
        flex-direction: column;
        padding: 0 60px 44px;
      }
      @media (max-width: 991px) {
        .div-16 {
          max-width: 100%;
          padding: 0 20px;
        }
      }
      .img-4 {
        aspect-ratio: 1.67;
        object-fit: contain;
        object-position: center;
        width: 90px;
      }
      .div-17 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        text-align: center;
        text-transform: uppercase;
        align-self: center;
        white-space: nowrap;
        font: 400 24px/129% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-17 {
          white-space: initial;
        }
      }
      .div-18 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        text-align: center;
        justify-content: center;
        align-items: center;
        margin-top: 10px;
        padding: 1px 60px;
        font: 400 16px/24px Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-18 {
          max-width: 100%;
          padding: 0 20px;
        }
      }
      .img-5 {
        aspect-ratio: 1.89;
        object-fit: contain;
        object-position: center;
        width: 376px;
        max-width: 100%;
        align-self: center;
        margin-top: 30px;
      }
      .div-19 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        text-align: center;
        justify-content: center;
        align-items: center;
        margin-top: 30px;
        padding: 0 60px 22px;
        font: 400 14px/21px Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-19 {
          max-width: 100%;
          padding: 0 20px;
        }
      }
      .div-20 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        text-align: center;
        text-transform: uppercase;
        justify-content: center;
        align-items: center;
        border: 1px solid
          var(
            --12700155001519199951171875-x-6775999755859375-default-lochmara,
            #0575ca
          );
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-lochmara,
          #0575ca
        );
        padding: 10px 60px;
        font: 400 12px/150% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-20 {
          max-width: 100%;
          padding: 0 20px;
        }
      }
      .column-2 {
        display: flex;
        flex-direction: column;
        line-height: normal;
        width: 50%;
        margin-left: 20px;
      }
      @media (max-width: 991px) {
        .column-2 {
          width: 100%;
        }
      }
      .div-21 {
        align-items: center;
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-gallery,
          #ebebeb
        );
        display: flex;
        flex-grow: 1;
        flex-direction: column;
        padding: 0 30px 30px;
      }
      @media (max-width: 991px) {
        .div-21 {
          max-width: 100%;
          margin-top: 20px;
          padding: 0 20px;
        }
      }
      .div-22 {
        justify-content: center;
        align-items: center;
        align-self: stretch;
        display: flex;
        flex-direction: column;
        padding: 0 60px 44px;
      }
      @media (max-width: 991px) {
        .div-22 {
          max-width: 100%;
          padding: 0 20px;
        }
      }
      .img-6 {
        aspect-ratio: 1.96;
        object-fit: contain;
        object-position: center;
        width: 106px;
        max-width: 100%;
      }
      .div-23 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        text-align: center;
        text-transform: uppercase;
        white-space: nowrap;
        font: 400 24px/129% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-23 {
          white-space: initial;
        }
      }
      .div-24 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        text-align: center;
        margin-top: 10px;
        white-space: nowrap;
        font: 400 16px/150% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-24 {
          white-space: initial;
        }
      }
      .img-7 {
        aspect-ratio: 1.89;
        object-fit: contain;
        object-position: center;
        width: 383px;
        max-width: 100%;
        margin-top: 37px;
      }
      .div-25 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        text-align: center;
        margin-top: 37px;
        font: 400 14px/21px Montserrat, sans-serif;
      }
      .div-26 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        text-align: center;
        text-transform: uppercase;
        justify-content: center;
        align-items: center;
        border: 1px solid
          var(--12700155001519199951171875-x-6775999755859375-default-red, #e60000);
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-red,
          #e60000
        );
        align-self: stretch;
        margin-top: 29px;
        padding: 10px 60px;
        font: 400 12px/150% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-26 {
          max-width: 100%;
          padding: 0 20px;
        }
      }
      .div-27 {
        align-content: flex-start;
        flex-wrap: wrap;
        margin-top: 55px;
        padding: 0 15px 40px;
      }
      @media (max-width: 991px) {
        .div-27 {
          max-width: 100%;
          padding-right: 20px;
          margin-top: 40px;
        }
      }
      .div-28 {
        gap: 20px;
        display: flex;
      }
      @media (max-width: 991px) {
        .div-28 {
          flex-direction: column;
          align-items: stretch;
          gap: 0px;
        }
      }
      .column-3 {
        display: flex;
        flex-direction: column;
        line-height: normal;
        width: 33%;
        margin-left: 0px;
      }
      @media (max-width: 991px) {
        .column-3 {
          width: 100%;
        }
      }
      .div-29 {
        align-self: stretch;
        display: flex;
        flex-grow: 1;
        flex-direction: column;
      }
      @media (max-width: 991px) {
        .div-29 {
          margin-top: 30px;
        }
      }
      .div-30 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        text-align: center;
        text-transform: uppercase;
        white-space: nowrap;
        justify-content: center;
        align-items: center;
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mine-shaft,
          #272727
        );
        padding: 9px 60px;
        font: 700 15px/150% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-30 {
          white-space: initial;
          padding: 0 20px;
        }
      }
      .div-31 {
        border-right: 0.8px solid
          var(--12700155001519199951171875-x-6775999755859375-default-silver, #ccc);
        border-bottom: 0.8px solid
          var(--12700155001519199951171875-x-6775999755859375-default-silver, #ccc);
        border-left: 0.8px solid
          var(--12700155001519199951171875-x-6775999755859375-default-silver, #ccc);
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mercury,
          #e6e6e6
        );
        display: flex;
        flex-direction: column;
        padding: 27px 10px 11px;
      }
      .img-8 {
        aspect-ratio: 0.68;
        object-fit: contain;
        object-position: center;
        width: 100px;
        max-width: 100%;
        align-self: center;
      }
      .div-32 {
        display: flex;
        margin-top: 16px;
        gap: 5px;
        font-size: 14px;
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        font-weight: 400;
        letter-spacing: -0.5px;
        padding: 8px 0;
      }
      .div-33 {
        font-family: Montserrat, sans-serif;
        line-height: 150%;
      }
      .div-34 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-ocean-green,
          #3cad86
        );
        font: 700 22px/150% Montserrat, sans-serif;
      }
      .div-35 {
        font-family: Montserrat, sans-serif;
        line-height: 150%;
        flex-grow: 1;
        flex-basis: auto;
      }
      .div-36 {
        align-items: start;
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mercury,
          #e6e6e6
        );
        display: flex;
        flex-direction: column;
        padding: 22px 80px 22px 20px;
      }
      @media (max-width: 991px) {
        .div-36 {
          padding-right: 20px;
        }
      }
      .div-37 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        justify-content: center;
        padding: 9px 0;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      .div-38 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        justify-content: center;
        padding: 9px 0;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      .div-39 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 60px 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-39 {
          white-space: initial;
          padding-right: 23px;
        }
      }
      .div-40 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 8px 2px 8px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-40 {
          white-space: initial;
        }
      }
      .div-41 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 19px 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-41 {
          white-space: initial;
        }
      }
      .div-42 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-42 {
          white-space: initial;
        }
      }
      .div-43 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        text-align: center;
        text-transform: uppercase;
        white-space: nowrap;
        justify-content: center;
        align-items: center;
        border: 1px solid
          var(
            --12700155001519199951171875-x-6775999755859375-default-keppel,
            #37b48f
          );
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-keppel,
          #37b48f
        );
        padding: 16px 60px;
        font: 400 12px/150% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-43 {
          white-space: initial;
          padding: 0 20px;
        }
      }
      .column-4 {
        display: flex;
        flex-direction: column;
        line-height: normal;
        width: 33%;
        margin-left: 20px;
      }
      @media (max-width: 991px) {
        .column-4 {
          width: 100%;
        }
      }
      .div-44 {
        align-self: stretch;
        display: flex;
        flex-grow: 1;
        flex-direction: column;
      }
      @media (max-width: 991px) {
        .div-44 {
          margin-top: 30px;
        }
      }
      .div-45 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        text-align: center;
        text-transform: uppercase;
        white-space: nowrap;
        justify-content: center;
        align-items: center;
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mine-shaft,
          #272727
        );
        padding: 9px 60px;
        font: 700 15px/150% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-45 {
          white-space: initial;
          padding: 0 20px;
        }
      }
      .div-46 {
        border-right: 0.8px solid
          var(--12700155001519199951171875-x-6775999755859375-default-silver, #ccc);
        border-bottom: 0.8px solid
          var(--12700155001519199951171875-x-6775999755859375-default-silver, #ccc);
        border-left: 0.8px solid
          var(--12700155001519199951171875-x-6775999755859375-default-silver, #ccc);
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mercury,
          #e6e6e6
        );
        display: flex;
        flex-direction: column;
        padding: 27px 11px 11px;
      }
      .img-9 {
        aspect-ratio: 0.68;
        object-fit: contain;
        object-position: center;
        width: 100px;
        max-width: 100%;
        align-self: center;
      }
      .div-47 {
        display: flex;
        margin-top: 16px;
        gap: 3px;
        font-size: 14px;
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        font-weight: 400;
        letter-spacing: -0.5px;
        padding: 8px 0;
      }
      .div-48 {
        font-family: Montserrat, sans-serif;
        line-height: 150%;
      }
      .div-49 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-ocean-green,
          #3cad86
        );
        font: 700 22px/150% Montserrat, sans-serif;
      }
      .div-50 {
        font-family: Montserrat, sans-serif;
        line-height: 150%;
        flex-grow: 1;
        flex-basis: auto;
      }
      .div-51 {
        align-items: start;
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mercury,
          #e6e6e6
        );
        display: flex;
        flex-direction: column;
        padding: 22px 80px 22px 20px;
      }
      @media (max-width: 991px) {
        .div-51 {
          padding-right: 20px;
        }
      }
      .div-52 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        justify-content: center;
        padding: 8px 0;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      .div-53 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        justify-content: center;
        padding: 9px 0;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      .div-54 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-54 {
          white-space: initial;
        }
      }
      .div-55 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 48px 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-55 {
          white-space: initial;
          padding-right: 20px;
        }
      }
      .div-56 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 1px 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-56 {
          white-space: initial;
        }
      }
      .div-57 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 2px 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-57 {
          white-space: initial;
        }
      }
      .div-58 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        text-align: center;
        text-transform: uppercase;
        white-space: nowrap;
        justify-content: center;
        align-items: center;
        border: 1px solid
          var(
            --12700155001519199951171875-x-6775999755859375-default-keppel,
            #37b48f
          );
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-keppel,
          #37b48f
        );
        padding: 16px 60px;
        font: 400 12px/150% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-58 {
          white-space: initial;
          padding: 0 20px;
        }
      }
      .column-5 {
        display: flex;
        flex-direction: column;
        line-height: normal;
        width: 33%;
        margin-left: 20px;
      }
      @media (max-width: 991px) {
        .column-5 {
          width: 100%;
        }
      }
      .div-59 {
        align-self: stretch;
        display: flex;
        flex-grow: 1;
        flex-direction: column;
      }
      @media (max-width: 991px) {
        .div-59 {
          margin-top: 30px;
        }
      }
      .div-60 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        text-align: center;
        text-transform: uppercase;
        white-space: nowrap;
        justify-content: center;
        align-items: center;
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mine-shaft,
          #272727
        );
        padding: 9px 60px;
        font: 700 15px/150% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-60 {
          white-space: initial;
          padding: 0 20px;
        }
      }
      .div-61 {
        border-right: 0.8px solid
          var(--12700155001519199951171875-x-6775999755859375-default-silver, #ccc);
        border-bottom: 0.8px solid
          var(--12700155001519199951171875-x-6775999755859375-default-silver, #ccc);
        border-left: 0.8px solid
          var(--12700155001519199951171875-x-6775999755859375-default-silver, #ccc);
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mercury,
          #e6e6e6
        );
        display: flex;
        flex-direction: column;
        padding: 27px 11px 11px;
      }
      .img-10 {
        aspect-ratio: 0.68;
        object-fit: contain;
        object-position: center;
        width: 100px;
        max-width: 100%;
        align-self: center;
      }
      .div-62 {
        display: flex;
        margin-top: 16px;
        gap: 4px;
        font-size: 14px;
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        font-weight: 400;
        letter-spacing: -0.5px;
        padding: 8px 0;
      }
      .div-63 {
        font-family: Montserrat, sans-serif;
        line-height: 150%;
      }
      .div-64 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-ocean-green,
          #3cad86
        );
        font: 700 22px/150% Montserrat, sans-serif;
      }
      .div-65 {
        font-family: Montserrat, sans-serif;
        line-height: 150%;
        flex-grow: 1;
        flex-basis: auto;
      }
      .div-66 {
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-mercury,
          #e6e6e6
        );
        display: flex;
        flex-direction: column;
        padding: 22px 64px 22px 20px;
      }
      @media (max-width: 991px) {
        .div-66 {
          padding-right: 20px;
        }
      }
      .div-67 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        justify-content: center;
        padding: 8px 0;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      .div-68 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        justify-content: center;
        padding: 9px 0;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      .div-69 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 35px 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-69 {
          white-space: initial;
          padding-right: 20px;
        }
      }
      .div-70 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 2px 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-70 {
          white-space: initial;
        }
      }
      .div-71 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        justify-content: center;
        padding: 9px 0;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      .div-72 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        white-space: nowrap;
        justify-content: center;
        padding: 9px 60px 9px 7px;
        font: 400 12px/208% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-72 {
          white-space: initial;
          padding-right: 20px;
        }
      }
      .div-73 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-nero,
          #fff
        );
        text-align: center;
        text-transform: uppercase;
        white-space: nowrap;
        justify-content: center;
        align-items: center;
        border: 1px solid
          var(
            --12700155001519199951171875-x-6775999755859375-default-keppel,
            #37b48f
          );
        background-color: var(
          --12700155001519199951171875-x-6775999755859375-default-keppel,
          #37b48f
        );
        padding: 16px 60px;
        font: 400 12px/150% Montserrat, sans-serif;
      }
      @media (max-width: 991px) {
        .div-73 {
          white-space: initial;
          padding: 0 20px;
        }
      }
      .div-74 {
        color: var(
          --12700155001519199951171875-x-6775999755859375-default-black,
          #000
        );
        width: 100%;
        font: 400 16px/150% Open Sans, sans-serif;
      }
      @media (max-width: 991px) {
        .div-74 {
          max-width: 100%;
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



/*BOTTONE AMD E INTEL*/
  button {
 position: relative;
 display: inline-block;
 cursor: pointer;
 outline: none;
 border: 0;
 vertical-align: middle;
 text-decoration: none;
 background: transparent;
 padding: 0;
 font-size: inherit;
 font-family: inherit;
}

button.learn-more {
 width: 12rem;
 height: auto;
}

button.learn-more .circle {
 transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
 position: relative;
 display: block;
 margin: 0;
 width: 3rem;
 height: 3rem;
 background: #282936;
 border-radius: 1.625rem;
}

button.learn-more .circle .icon {
 transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
 position: absolute;
 top: 0;
 bottom: 0;
 margin: auto;
 background: #fff;
}

button.learn-more .circle .icon.arrow {
 transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
 left: 0.625rem;
 width: 1.125rem;
 height: 0.125rem;
 background: none;
}

button.learn-more .circle .icon.arrow::before {
 position: absolute;
 content: "";
 top: -0.29rem;
 right: 0.0625rem;
 width: 0.625rem;
 height: 0.625rem;
 border-top: 0.125rem solid #fff;
 border-right: 0.125rem solid #fff;
 transform: rotate(45deg);
}

button.learn-more .button-text {
 transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
 position: absolute;
 top: 0;
 left: 0;
 right: 0;
 bottom: 0;
 padding: 0.75rem 0;
 margin: 0 0 0 1.85rem;
 color: #282936;
 font-weight: 700;
 line-height: 1.6;
 text-align: center;
 text-transform: uppercase;
}

button:hover .circle {
 width: 100%;
}

button:hover .circle .icon.arrow {
 background: #fff;
 transform: translate(1rem, 0);
}

button:hover .button-text {
 color: #fff;
}




/*BOTTONI PER LA CONFIGURAZIONE DEI 3 PC A FINE PAGINA*/
#bottone1 {
 padding-left: 33px;
 padding-right: 33px;
 padding-bottom: 16px;
 padding-top: 16px;
 border-radius: 9px;
 background: #d5f365;
 border: none;
 font-family: inherit;
 text-align: center;
 cursor: pointer;
 transition: 0.4s;
}

#bottone1:hover {
 box-shadow: 7px 5px 56px -14px #C3D900;
}

#bottone1:active {
 transform: scale(0.97);
 box-shadow: 7px 5px 56px -10px #C3D900;
}

    </style>

