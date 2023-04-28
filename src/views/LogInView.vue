<template>
  <div class="website">
    <!-- Navbar (sit on top) -->
    <div class="w3-top">
      <div class="w3-bar w3-white w3-card" id="myNavbar">
        <a href="#home" class="w3-bar-item w3-button w3-wide"
          ><img
            style="height: 40px; width: 108px"
            src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/logoFull.png"
            alt="logo"
        /></a>
        <!-- Right-sided navbar links -->
        <div class="w3-right w3-hide-small">
          <a href="#about" class="w3-bar-item w3-button">Sobre mí</a>
          <a href="#team" class="w3-bar-item w3-button"
            ><i class="fas fa-map-marker-alt"></i> #VisitaDeLaSalud</a
          >
          <a href="#work" class="w3-bar-item w3-button"
            ><i class="fas fa-handshake"></i> Únete</a
          >
          <a href="#pricing" class="w3-bar-item w3-button"
            ><i class="fas fa-certificate"></i> Colaboradores</a
          >
          <a href="#contact" class="w3-bar-item w3-button"
            ><i class="fa fa-envelope"></i> Contacto</a
          >
        </div>
        <!-- Hide right-floated links on small screens and replace them with a menu icon -->

        <a
          href="javascript:void(0)"
          class="w3-bar-item w3-button w3-right w3-hide-large w3-hide-medium"
          onclick="w3_open()"
        >
          <i @click="openMenu()" class="fa fa-bars"></i>
        </a>
      </div>
    </div>

    <!-- Sidebar on small screens when clicking the menu icon -->
    <nav
      class="w3-sidebar w3-bar-block w3-black w3-card w3-animate-left w3-hide-medium w3-hide-large"
      :style="this.navDisplay"
      id="mySidebar"
    >
      <a
        @click="closeMenu()"
        href="javascript:void(0)"
        onclick="w3_close()"
        class="w3-bar-item w3-button w3-large w3-padding-16"
        >Cerrar x</a
      >
      <a @click="closeMenu()" href="#about" class="w3-bar-item w3-button"
        >Sobre mí</a
      >
      <a @click="closeMenu()" href="#team" class="w3-bar-item w3-button"
        ><i class="fas fa-map-marker-alt"></i> #VisitaDeLaSalud</a
      >
      <a @click="closeMenu()" href="#work" class="w3-bar-item w3-button"
        ><i class="fas fa-handshake"></i> Únete</a
      >
      <a @click="closeMenu()" href="#pricing" class="w3-bar-item w3-button"
        ><i class="fas fa-certificate"></i> Colaboradores</a
      >
      <a @click="closeMenu()" href="#contact" class="w3-bar-item w3-button"
        ><i class="fa fa-envelope"></i> Contacto</a
      >
    </nav>

    <!-- Header with full-height image -->
    <header class="bgimg-1 w3-display-container-min" id="home">
      <div class="w3-display-left w3-text-white" style="padding:48px">
        <span class="w3-jumbo w3-hide-small myPhrase"
          >La salud es un derecho, <br />
          no un privilegio</span
        ><br />
        <span class="w3-xxlarge w3-hide-large w3-hide-medium myPhrase"
          >La salud es un derecho, <br />
          no un privilegio
        </span>
        <br />
        <!-- <span class="w3-large"
          >Stop wasting valuable time with projects that just isn't you.</span
        > -->
        <p>
          <!-- <a
            href="#about"
            class="w3-button w3-white w3-padding-large w3-large w3-margin-top w3-opacity w3-hover-opacity-off"
            >Conocer más</a
          > -->

          <button
            class="mineButton w3-button w3-padding-large w3-large w3-margin-top"
          >
            Conocer más
          </button>
        </p>
      </div>
      <div
        class="w3-display-bottomleft w3-text-grey w3-large"
        style="padding:24px 48px"
      >
        <i
          style=" cursor: pointer"
          class="fa fa-facebook-official w3-hover-opacity"
        ></i>
        <i
          style=" cursor: pointer"
          class="fa fa-instagram w3-hover-opacity"
        ></i>
        <i style=" cursor: pointer" class="fa fa-twitter w3-hover-opacity"></i>
      </div>
    </header>

    <!-- About Section -->
    <!-- <div class="w3-container" style="padding:128px 16px" id="about">
      <h3 class="w3-center">Sobre mí</h3>
      <p class="w3-center w3-large">Director General de la Clínica
y Fundación Cruz Jiminian</p>
      <div class="w3-row-padding w3-center" style="margin-top:64px">
        <div class="w3-quarter">
          <i class="fa fa-desktop w3-margin-bottom w3-jumbo w3-center"></i>
          <p class="w3-large">Responsive</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore.
          </p>
        </div>
        <div class="w3-quarter">
          <i class="fa fa-heart w3-margin-bottom w3-jumbo"></i>
          <p class="w3-large">Passion</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore.
          </p>
        </div>
        <div class="w3-quarter">
          <i class="fa fa-diamond w3-margin-bottom w3-jumbo"></i>
          <p class="w3-large">Design</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore.
          </p>
        </div>
        <div class="w3-quarter">
          <i class="fa fa-cog w3-margin-bottom w3-jumbo"></i>
          <p class="w3-large">Support</p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore.
          </p>
        </div>
      </div>
    </div> -->

    <!-- Promo Section - "We know design" -->
    <div
      class="w3-container myBackground"
      style="padding:128px 16px"
      id="about"
    >
      <div class="w3-row-padding">
        <div class="w3-col m6">
          <img
            class="w3-image w3-round-large"
            src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/sobreMi.png"
            alt="Buildings"
            width="700"
            height="394"
          />
        </div>
        <div class="w3-col m6">
          <h3 style="font-weight: bold; font-size: 30px">Sobre mí</h3>
          <!-- <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod<br />tempor incididunt ut labore et dolore.
          </p> -->
          <p class="myCard">
            <span>
              Director General de la Clínica
            </span>
            <br />
            <span>
              y Fundación Cruz Jiminián
            </span>
          </p>
          <p style="font-weight: bold; font-size: 17px">
            Apasionado con el impacto social y lo humano. Soy médico
            epidemiólogo y actualmente funjo como Subdirector General de la
            Clínica Cruz Jiminián y la Fundación Cruz Jiminián, además de
            desempeñar el puesto de Director Médico de Atención Primarias UNISAF
            y Director de CEOM/ Oncología. He recorrido todo el país junto a mi
            equipo de trabajo, dirigiendo más de 200 Operativos Médicos y
            Jornadas de Salud que han impactado a más de 50,000 dominicanos.
            Estudié en la Academia Militar Riverside en Atlanta, Georgia. Más
            adelante, ingreso a la carrera de Medicina en la Universidad
            Iberoamericana (UNIBE). También me he capacitado en Gerencia
            Hospitalaria y Seguridad, Asistencia Quirúrgica, Auditoría Médica y
            Lenguaje de Señas enfocado en Medicina. Mi labor social no se limita
            solo al área de salud, sino que también he desarrollado programas de
            asistencia que han impactado a niños huérfanos, mujeres maltratadas,
            envejecientes, madres solteras, jóvenes deportistas y comunidades
            afectadas por desastres naturales. Mi mayor convicción es apoyar a
            las personas que carecen de recursos económicos y no tienen los
            medios necesarios para acceder a una asistencia de salud digna o la
            mejor calidad de vida que merecen.
          </p>
          <button
            class="mineButton w3-button w3-padding-large w3-large w3-margin-top"
          >
            Conocer más
          </button>
          <!-- <img
            style="width: 150px; position: relative; top: -650px; left: 400px;"
            src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/iconHealth.png"
          /> -->
          <!-- <img
            style="width: 150px; position: relative; top: 335px; left: -1030px;"
            src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/iconHelp.png"
          /> -->
        </div>
      </div>
    </div>

    <!-- Promo Section "Statistics" -->
    <div class="w3-container w3-row w3-center w3-padding-64 myBand">
      <div class="w3-quarter">
        <span class="w3-xxlarge">+200</span>
        <br />Operativos médicos coordinados
      </div>
      <div class="w3-quarter">
        <span class="w3-xxlarge">+1,250</span>
        <br />Causas sociales entregadas
      </div>
      <div class="w3-quarter">
        <span class="w3-xxlarge">+125</span>
        <br />Voluntarios Registrados
      </div>
      <div class="w3-quarter">
        <span class="w3-xxlarge">+5</span>
        <br />Instituciones Colaboradoras
      </div>
    </div>

    <!-- Promo Section - "We know design" -->
    <div class="w3-container" style="padding:128px 16px" id="team">
      <div class="w3-row-padding">
        <div class="w3-col m6">
          <h3 style="font-weight: bold; font-size: 30px">#VisitaDeLaSalud</h3>
          <p class="myCard">
            <span>
              Años de labor social
            </span>
            <br />
            <span>
              me han llevado a crear este sueño
            </span>
          </p>
          <p style="font-weight: bold; font-size: 17px">
            La Visita de la Salud es una iniciativa que he creado con el fin de
            recorrer todo el territorio nacional, visitando las 32 provincias e
            identificando casos de emergencia o pobreza que requieran asistencia
            médica. En este proyecto busco devolver la salud a quienes más lo
            necesitan a través de un servicio médico digno y la enorme vocación
            de servicio que siempre nos ha caracterizado. Estaremos tocando la
            puerta de personas enfermas, en cama o con alguna capacidad especial
            que no puedan ir a un operativo o centro médico. Esta iniciativa
            cuenta con el apoyo de instituciones tanto públicas y privadas como
            OMSA, Comedores Económicos, Mejía Arcalá, Comisión Barrial, Sael
            Pañales, entre otros.
          </p>
          <button
            class="mineButton w3-button w3-padding-large w3-large w3-margin-top"
          >
            Conocer más
          </button>
        </div>
        <div class="w3-col m6">
          <!-- <img
            class="w3-image w3-round-large"
            src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/sobreMi.png"
            alt="Buildings"
            width="700"
            height="394"
          /> -->
        </div>
      </div>
    </div>

    <!-- Pricing Section -->
    <div
      class="w3-container w3-center myBackground"
      style="padding:128px 16px"
      id="work"
    >
      <!-- <img
        style="width: 150px; position: relative; top: 0px; left: 0px;"
        src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/iconHealth.png"
      />
      <img
        style="width: 150px; position: relative; top: 0px; left: 0px;"
        src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/iconHelp.png"
      /> -->
      <h3 style="font-weight: bold; font-size: 30px">Únete</h3>
      <div class="w3-row-padding" style="margin-top:64px">
        <div class="w3-third w3-section">
          <ul class="w3-ul myBorder w3-hover-shadow">
            <img
              style="border-radius: 50%; width: 150px; height: 150px; position: relative; top: 20px; left: 0px;"
              src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/join-cause.jpg"
            />
            <li class="myBorder w3-xlarge w3-padding-32">Registra tu causa</li>
            <li class="w3-padding-16">
              Ahora tienes la oportunidad de explicarme tu caso
            </li>

            <li class="myBorder w3-padding-24">
              <button class="w3-button w3-black w3-padding-large">
                Unirme
              </button>
            </li>
          </ul>
        </div>
        <div class="w3-third">
          <ul class="w3-ul w3-white w3-hover-shadow">
            <img
              style="border-radius: 50%; width: 150px; height: 150px; position: relative; top: 20px; left: 0px;"
              src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/join-volunteer.jpg"
            />
            <li class="w3-xlarge w3-padding-48">
              Sé parte de nuestro voluntariado
            </li>
            <li class="w3-padding-16">
              Si tienes disponibilidad, puedes ser parte de nuestra labor social
            </li>

            <li class="w3-white w3-padding-24">
              <button class="w3-button w3-black w3-padding-large">
                Unirme
              </button>
            </li>
          </ul>
        </div>
        <div class="w3-third w3-section">
          <ul class="w3-ul myBorder w3-hover-shadow">
            <img
              style="border-radius: 50%; width: 150px; height: 150px; position: relative; top: 20px; left: 0px;"
              src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/join-give.jpg"
            />
            <li class="myBorder w3-xlarge w3-padding-32">
              Contribuye con nuestra labor
            </li>
            <li class="w3-padding-16">
              Puedes donar recursos financieros, bienes o recursos
            </li>

            <li class="myBorder w3-padding-24">
              <button class="w3-button w3-black w3-padding-large">
                Unirme
              </button>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <!-- Work Section -->
    <div class="w3-container" style="padding:128px 16px" id="work">
      <h3 class="w3-center" style="font-weight: bold; font-size: 30px">
        Redes Sociales
      </h3>
      <div class="w3-row-padding" style="margin-top:64px">
        <div class="w3-col l3 m6"></div>
        <div class="w3-col l3 m6"></div>
        <div class="w3-col l3 m6"></div>
        <div class="w3-col l3 m6"></div>
      </div>

      <!-- <div class="w3-row-padding w3-section">
        <div class="w3-col l3 m6">
          <img
            src="/w3images/tech_tablet.jpg"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="A tablet"
          />
        </div>
        <div class="w3-col l3 m6">
          <img
            src="/w3images/tech_camera.jpg"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="A camera"
          />
        </div>
        <div class="w3-col l3 m6">
          <img
            src="/w3images/tech_typewriter.jpg"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="A typewriter"
          />
        </div>
        <div class="w3-col l3 m6">
          <img
            src="/w3images/tech_tableturner.jpg"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="A tableturner"
          />
        </div>
      </div> -->
    </div>

    <!-- Contact Section -->
    <div
      class="w3-container myBackgroundCrema"
      style="padding:128px 16px"
      id="update"
    >
      <h3 class="w3-center" style="font-weight: bold; font-size: 30px">
        Actualízate con nuestros operativos, causas y más...
      </h3>
      <div style="margin-top:48px">
        <br />
        <form action="/action_page.php" target="_blank" class="grid">
          <p>
            <input
              class="w3-input w3-border"
              type="text"
              placeholder="Name"
              required
              name="Name"
            />
          </p>
          <p>
            <input
              class="w3-input w3-border"
              type="text"
              placeholder="Email"
              required
              name="Email"
            />
          </p>
          <p>
            <button class="w3-button w3-black" type="submit">
              <i class="fa fa-paper-plane"></i> Enviar
            </button>
          </p>
        </form>
      </div>
    </div>

    <div class="w3-container" id="work">
      <!-- <h3 class="w3-center" style="font-weight: bold; font-size: 30px">Redes Sociales</h3> -->
      <div class="w3-row-padding">
        <div class="w3-col l3 m6">
          <img
            src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/ig-1.JPG"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="Operativo de Salud Mental"
          />
        </div>
        <div class="w3-col l3 m6">
          <img
            src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/ig-2.JPG"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="Visita a Niños"
          />
        </div>
        <div class="w3-col l3 m6">
          <img
            src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/ig-3.JPG"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="Entrega de Medicamentos"
          />
        </div>
        <div class="w3-col l3 m6">
          <img
            src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/ig-4.JPG"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="Presentación"
          />
        </div>
      </div>

      <!-- <div class="w3-row-padding w3-section">
        <div class="w3-col l3 m6">
          <img
            src="/w3images/tech_tablet.jpg"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="A tablet"
          />
        </div>
        <div class="w3-col l3 m6">
          <img
            src="/w3images/tech_camera.jpg"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="A camera"
          />
        </div>
        <div class="w3-col l3 m6">
          <img
            src="/w3images/tech_typewriter.jpg"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="A typewriter"
          />
        </div>
        <div class="w3-col l3 m6">
          <img
            src="/w3images/tech_tableturner.jpg"
            style="width:100%"
            onclick="onClick(this)"
            class="w3-hover-opacity"
            alt="A tableturner"
          />
        </div>
      </div> -->
    </div>

    <!-- Modal for full size images on click-->
    <div
      id="modal01"
      class="w3-modal w3-black"
      onclick="this.style.display='none'"
    >
      <span
        class="w3-button w3-xxlarge w3-black w3-padding-large w3-display-topright"
        title="Close Modal Image"
        >×</span
      >
      <div
        class="w3-modal-content w3-animate-zoom w3-center w3-transparent w3-padding-64"
      >
        <img id="img01" class="w3-image" />
        <p id="caption" class="w3-opacity w3-large"></p>
      </div>
    </div>

    <!-- Team Section -->
    <div class="w3-container" style="padding:128px 16px" id="pricing">
      <h3 style="font-weight: bold; font-size: 30px" class="w3-center">
        Colaboradores
      </h3>
      <p class="w3-center w3-large">
        Los que contribuyen a que esto sea posible
      </p>
      <div class="w3-row-padding" style="margin-top:64px">
        <div class="w3-col l3 m6 w3-margin-bottom">
          <div class="w3-card">
            <img
              src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/colab-CCJ.png"
              alt="John"
              style="width:100%"
            />
            <div class="w3-container">
              <h4>Clínica Cruz Jiminián</h4>
              <p class="w3-opacity">Centro de Salud</p>
              <p>
                Phasellus eget enim eu lectus faucibus vestibulum. Suspendisse
                sodales pellentesque elementum.
              </p>
              <p>
                <button class="w3-button w3-light-grey w3-block">
                  <i class="fa fa-envelope"></i> Contact
                </button>
              </p>
            </div>
          </div>
        </div>
        <div class="w3-col l3 m6 w3-margin-bottom">
          <div class="w3-card">
            <img
              src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/colab-mejiaAlcala.png"
              alt="Jane"
              style="width:100%"
            />
            <div class="w3-container">
              <h4>Grupo Mejía Alcalá</h4>
              <p class="w3-opacity">Productos de Alta Calidad</p>
              <p>
                Phasellus eget enim eu lectus faucibus vestibulum. Suspendisse
                sodales pellentesque elementum.
              </p>
              <p>
                <button class="w3-button w3-light-grey w3-block">
                  <i class="fa fa-envelope"></i> Contact
                </button>
              </p>
            </div>
          </div>
        </div>
        <div class="w3-col l3 m6 w3-margin-bottom">
          <div class="w3-card">
            <img
              src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/colab-comBarrial.jpg"
              alt="Mike"
              style="width:100%"
            />
            <div class="w3-container">
              <h4>Comisión Barrial</h4>
              <p class="w3-opacity">Organismo Gubernamental</p>
              <p>
                Phasellus eget enim eu lectus faucibus vestibulum. Suspendisse
                sodales pellentesque elementum.
              </p>
              <p>
                <button class="w3-button w3-light-grey w3-block">
                  <i class="fa fa-envelope"></i> Contact
                </button>
              </p>
            </div>
          </div>
        </div>
        <div class="w3-col l3 m6 w3-margin-bottom">
          <div class="w3-card">
            <img
              src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/colab-fundCJ.png"
              alt="Dan"
              style="width:100%"
            />
            <div class="w3-container">
              <h4>Fundación Cruz Jiminián</h4>
              <p class="w3-opacity">Fundación de Salud</p>
              <p>
                Phasellus eget enim eu lectus faucibus vestibulum. Suspendisse
                sodales pellentesque elementum.
              </p>
              <p>
                <button class="w3-button w3-light-grey w3-block">
                  <i class="fa fa-envelope"></i> Contact
                </button>
              </p>
            </div>
          </div>
        </div>
        <div class="w3-col l3 m6 w3-margin-bottom">
          <div class="w3-card">
            <img
              src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/colab-comEconomicos.jpg"
              alt="Dan"
              style="width:100%"
            />
            <div class="w3-container">
              <h4>Comedores Económicos</h4>
              <p class="w3-opacity">Alimentos de Calidad</p>
              <p>
                Phasellus eget enim eu lectus faucibus vestibulum. Suspendisse
                sodales pellentesque elementum.
              </p>
              <p>
                <button class="w3-button w3-light-grey w3-block">
                  <i class="fa fa-envelope"></i> Contact
                </button>
              </p>
            </div>
          </div>
        </div>
        <div class="w3-col l3 m6 w3-margin-bottom">
          <div class="w3-card">
            <img
              src="https://isys-assets-bucket.s3.amazonaws.com/luiscruzrd/colab-omsa.jpg"
              alt="Dan"
              style="width:100%"
            />
            <div class="w3-container">
              <h4>OMSA</h4>
              <p class="w3-opacity">Servicios de Transporte</p>
              <p>
                Phasellus eget enim eu lectus faucibus vestibulum. Suspendisse
                sodales pellentesque elementum.
              </p>
              <p>
                <button class="w3-button w3-light-grey w3-block">
                  <i class="fa fa-envelope"></i> Contact
                </button>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Team Section -->
    <div
      class="w3-container myBackground"
      style="padding:128px 16px; padding-bottom: 0"
      id="contact"
    >
      <h3 style="font-weight: bold; font-size: 30px" class="w3-center">
        Contacto
      </h3>
      <p style="color: black" class="w3-center w3-large">
        <span style="font-weight: bold">Correo:</span> luiscruzccj@gmail.com
      </p>
      <p style="color: black" class="w3-center w3-large">
        <span style="font-weight: bold">Teléfono:</span> (809) 707-1543
      </p>
      <p style="color: black" class="w3-center w3-large">
        <span style="font-weight: bold">Dirección:</span> Cristo Rey, Av. Ortega
        y Gasset 115-129, Santo Domingo
      </p>
      <p class="w3-center w3-large">
        <i
          style="font-size: 150px; color: black "
          class="fas fa-ellipsis-h"
        ></i>
      </p>
    </div>

    <!-- Skills Section -->
    <!-- <div class="w3-container w3-light-grey w3-padding-64">
      <div class="w3-row-padding">
        <div class="w3-col m6">
          <h3>Our Skills.</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod<br />
            tempor incididunt ut labore et dolore.
          </p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod<br />
            tempor incididunt ut labore et dolore.
          </p>
        </div>
        <div class="w3-col m6">
          <p class="w3-wide">
            <i class="fa fa-camera w3-margin-right"></i>Photography
          </p>
          <div class="w3-grey">
            <div class="w3-container w3-dark-grey w3-center" style="width:90%">
              90%
            </div>
          </div>
          <p class="w3-wide">
            <i class="fa fa-desktop w3-margin-right"></i>Web Design
          </p>
          <div class="w3-grey">
            <div class="w3-container w3-dark-grey w3-center" style="width:85%">
              85%
            </div>
          </div>
          <p class="w3-wide">
            <i class="fa fa-photo w3-margin-right"></i>Photoshop
          </p>
          <div class="w3-grey">
            <div class="w3-container w3-dark-grey w3-center" style="width:75%">
              75%
            </div>
          </div>
        </div>
      </div>
    </div> -->

    <!-- Footer -->
    <footer class="w3-center w3-black w3-padding-64">
      <a href="#home" class="w3-button w3-light-grey"
        ><i class="fa fa-arrow-up w3-margin-right"></i>Ir al Inicio</a
      >
      <div class="w3-xlarge w3-section">
        <i
          style=" cursor: pointer"
          class="fa fa-facebook-official w3-hover-opacity"
        ></i>
        <i
          style=" cursor: pointer"
          class="fa fa-instagram w3-hover-opacity"
        ></i>
        <i style=" cursor: pointer" class="fa fa-twitter w3-hover-opacity"></i>
      </div>
    </footer>
  </div>
</template>

<script lang="ts">
export default {
  name: "LoginView",
  components: {},

  data() {
    return {
      navDisplay: "display:none",
    };
  },

  methods: {
    closeMenu() {
      this.navDisplay = "display:none";
    },

    openMenu() {
      if (this.navDisplay === "display:block") {
        this.navDisplay = "display:none";
      } else {
        this.navDisplay = "display:block";
      }
    },
  },
};
</script>

<style lang="css" scoped>
.mineButton {
  background-color: rgb(193, 142, 97);
  color: white;
}

.myPhrase {
  font-weight: bold;
}

.myBackgroundCrema {
  background-color: rgb(193, 142, 97);
}

.myBackground {
  background-color: rgb(183, 201, 207);
}

.myCard {
  background-color: rgb(193, 142, 97);
  padding: 18px;
  /* width: 350px; */
  font-weight: bold;
  color: black;
}

.myBand {
  background-color: rgb(193, 142, 97);
  font-weight: bold;
  color: white;
}

.myBorder {
  background-color: rgb(193, 142, 97);
}

.grid {
  display: grid;
  grid-auto-flow: dense;
  grid-template-rows: auto auto;
  gap: 3px;
  grid-template-columns: repeat(auto-fit, minmax(13rem, 1fr));
  margin-left: 20%;
}
</style>
