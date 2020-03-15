<template>
  <div class="container-fluid">

    <!-- START NAV -->
    <nav class="navbar is-white">
      <div class="container">
        <div class="navbar-brand">
          <a class="navbar-item brand-text" href="../index.html">
            Bulma Admin
          </a>
          <div class="navbar-burger burger" data-target="navMenu">
            <span></span>
            <span></span>
            <span></span>
          </div>
        </div>
        <div id="navMenu" class="navbar-menu">
          <div class="navbar-start">
            <a class="navbar-item" href="admin.html">
              Home
            </a>
            <a class="navbar-item" href="admin.html">
              Orders
            </a>
            <a class="navbar-item" href="admin.html">
              Payments
            </a>
            <a class="navbar-item" href="admin.html">
              Exceptions
            </a>
            <a class="navbar-item" href="admin.html">
              Reports
            </a>
          </div>

        </div>
      </div>
    </nav>
    <!-- END NAV -->
    <div class="container">
      <div class="columns">

        <div class="column is-12">
          <!-- <nav class="breadcrumb" aria-label="breadcrumbs">
            <ul>
              <li><a href="../">Bulma</a></li>
              <li><a href="../">Templates</a></li>
              <li><a href="../">Examples</a></li>
              <li class="is-active"><a href="#" aria-current="page">Admin</a></li>
            </ul>
          </nav> -->
          <section class="hero is-info welcome is-small" style="position:relative; border-radius:10px; -webkit-box-shadow: 10px 10px 39px -6px rgba(0,0,0,0.75);
-moz-box-shadow: 10px 10px 39px -6px rgba(0,0,0,0.75);
box-shadow: 10px 10px 39px -6px rgba(0,0,0,0.75);">
            <div class="hello" ref="chartdiv"></div>
            <div class="" style="position:absolute;z-index:3;top:10px;left:10px">
              <div class="container">
                <h1 class="title is-marginless">
                  COVID 19 Information Board
                </h1>
                <small>by<a href="https://github.com/recitogigih" target="_blank" style="color:white"> Recito Gigih
                    P</a></small>
              </div>

            </div>
            <h2 class="subtitle" style="position:absolute;bottom:10px;left:10px;z-index:9">
              {{date}} <br> Last Update : {{lastUpdate}}
            </h2>
          </section>
          <br>
          <!-- <div class="hello" ref="chartdiv"></div> -->
          <section class="info-tiles">
            <div class="tile is-ancestor has-text-centered">
              <div class="tile is-parent">
                <article class="tile is-child box">
                  <p class="title has-text-info">{{ confirmed}}</p>
                  <p class="subtitle has-text-info">Confirmed</p>
                </article>
              </div>
              <div class="tile is-parent">
                <article class="tile is-child box">
                  <p class="title has-text-success">{{recovered}} <span class="subtitle has-text-success">
                      ({{percentageRecovered}}%) </span></p>
                  <p class="subtitle has-text-success">Recovered</p>
                </article>
              </div>
              <div class="tile is-parent">
                <article class="tile is-child box">
                  <p class="title has-text-danger">{{deaths}} <span class="subtitle has-text-danger">
                      ({{percentageDeaths}}%) </span> </p>
                  <p class="subtitle has-text-danger">Deaths</p>
                </article>
              </div>
              <div class="tile is-parent">
                <article class="tile is-child box">
                  <p class="title">{{treated}} <span class="subtitle "> ({{percentageTreated}}%) </span></p>
                  <p class="subtitle">Being treated</p>
                </article>
              </div>
            </div>
          </section>
          <div class="columns">
            <div class="column is-3">
              <div class="card events-card">
                <header class="card-header">
                  <p class="card-header-title">
                    Confirmed by Country
                  </p>
                  <a href="#" class="card-header-icon" aria-label="more options">
                    <span class="icon">
                      <i class="fa fa-angle-down" aria-hidden="true"></i>
                    </span>
                  </a>
                </header>
                <div class="card-table">
                  <div class="content">
                    <table class="table is-fullwidth is-striped">
                      <tbody>
                        <tr v-for="(confirmByCountry,index) in confirmByCountries" :key="index">
                          <td>
                            <country-flag :country=confirmByCountry.iso2 size='small' />
                          </td>
                          <td>{{confirmByCountry.countryRegion}} <span v-if="confirmByCountry.provinceState != null"> -
                              {{confirmByCountry.provinceState}}</span> </td>
                          <td class="has-text-centered">
                            <span class="tag is-link is-normal">{{zz[index]}}</span></td>
                          <td class="has-text-info">{{arrConfirmPercentage[index]}}% </td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </div>
                <footer class="card-footer">
                  <a href="#" class="card-footer-item">View All</a>
                </footer>
              </div>
            </div>
            <div class="column is-3">
              <div class="card events-card">
                <header class="card-header">
                  <p class="card-header-title">
                    Recovered by Country
                  </p>
                  <a href="#" class="card-header-icon" aria-label="more options">
                    <span class="icon">
                      <i class="fa fa-angle-down" aria-hidden="true"></i>
                    </span>
                  </a>
                </header>
                <div class="card-table">
                  <div class="content">
                    <table class="table is-fullwidth is-striped">
                      <tbody>
                        <tr v-for="(recoveredByCountry,index) in recoveredByCountries" :key="index">
                          <td width="5%">
                            <country-flag :country=recoveredByCountry.iso2 size='small' />
                          </td>
                          <td>{{recoveredByCountry.countryRegion}} <span
                              v-if="recoveredByCountry.provinceState != null"> -
                              {{recoveredByCountry.provinceState}}</span> </td>
                          <td class="has-text-centered">
                            <span class="tag is-success is-normal">{{recoveredByCountry.recovered}}</span></td>
                          <td class="has-text-success">{{arrRecoveredPercentage[index]}}% </td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </div>
                <footer class="card-footer">
                  <a href="#" class="card-footer-item">View All</a>
                </footer>
              </div>
            </div>
            <div class="column is-3">
              <div class="card events-card">
                <header class="card-header">
                  <p class="card-header-title">
                    Deaths by Country
                  </p>
                  <a href="#" class="card-header-icon" aria-label="more options">
                    <span class="icon">
                      <i class="fa fa-angle-down" aria-hidden="true"></i>
                    </span>
                  </a>
                </header>
                <div class="card-table">
                  <div class="content">
                    <table class="table is-fullwidth is-striped">
                      <tbody>
                        <tr v-for="(deathByCountry,index) in deathByCountries" :key="index">
                          <td width="5%">
                            <country-flag :country=deathByCountry.iso2 size='small' />
                          </td>
                          <td>{{deathByCountry.countryRegion}} <span v-if="deathByCountry.provinceState != null"> -
                              {{deathByCountry.provinceState}}</span> </td>
                          <td class="has-text-centered">

                            <span class="tag is-danger is-normal">{{deathByCountry.deaths}}</span>
                          </td>
                          <td class="has-text-danger">{{arrDeathPercentage[index]}}% </td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </div>
                <footer class="card-footer">
                  <a href="#" class="card-footer-item">View All</a>
                </footer>
              </div>
            </div>
            <div class="column is-3">
              <div class="card events-card">
                <header class="card-header">
                  <p class="card-header-title">
                    Events
                  </p>
                  <a href="#" class="card-header-icon" aria-label="more options">
                    <span class="icon">
                      <i class="fa fa-angle-down" aria-hidden="true"></i>
                    </span>
                  </a>
                </header>
                <div class="card-table">
                  <div class="content">
                    <table class="table is-fullwidth is-striped">
                      <tbody>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>


                      </tbody>
                    </table>
                  </div>
                </div>
                <footer class="card-footer">
                  <a href="#" class="card-footer-item">View All</a>
                </footer>
              </div>
            </div>

          </div>
        </div>
      </div>

      <div class="columns">
        <div class="column is-12">

          <div class="wrapper" style="height:500px; overflow:auto">
            <table class="table is-fullwidth is-hoverable table is-striped">
              <thead>
                <tr>
                  <th
                    style='position: sticky; top: -1px;background: #5B86E5;color:white;z-index:2;border-bottom:2px solid white'>
                    No</th>
                  <th
                    style='position: sticky; top: -1px;background: #5B86E5;color:white;z-index:2;border-bottom:2px solid white'>
                    Country</th>
                  <th
                    style='position: sticky; top: -1px;background: #5B86E5;color:white;z-index:2;border-bottom:2px solid white'>
                    Province State</th>
                  <th
                    style='position: sticky; top: -1px;background: #5B86E5;color:white;z-index:2;border-bottom:2px solid white'>
                    Confirmed</th>
                  <th
                    style='position: sticky; top: -1px;background: #5B86E5;color:white;z-index:2;border-bottom:2px solid white'>
                    Recovered</th>
                  <th
                    style='position: sticky; top: -1px;background: #5B86E5;color:white;z-index:2;border-bottom:2px solid white'>
                    Deaths</th>
                  <th
                    style='position: sticky; top: -1px;background: #5B86E5;color:white;z-index:2;border-bottom:2px solid white'>
                    Being Treated</th>
                  <th
                    style='position: sticky; top: -1px;background: #5B86E5;color:white;z-index:2;border-bottom:2px solid white'>
                    Recovery Rate</th>
                  <th
                    style='position: sticky; top: -1px;background: #5B86E5;color:white;z-index:2;border-bottom:2px solid white'>
                    Fatality Rate</th>
                </tr>
              </thead>
              <!-- <tfoot>
                <th><abbr title="Position">No</abbr></th>
                <th>Country</th>
                <th>Province State</th>
                <th><abbr title="Played">Confirmed</abbr></th>
                <th><abbr title="Won">Recovered</abbr></th>
                <th><abbr title="Drawn">Deaths</abbr></th>
                <th><abbr title="Lost">Being Treated</abbr></th>
                <th><abbr title="Goals for">Recovery Rate</abbr></th>
                <th><abbr title="Goals against">Fatality Rate</abbr></th>
            </tfoot> -->
              <tbody style="height:300px;">
                <tr v-for="(confirmByCountry,index) in confirmByCountries" :key="index">
                  <th>{{index+1}}</th>
                  <td>
                    <country-flag :country=confirmByCountry.iso2 size='small' />
                    {{confirmByCountry.countryRegion}}
                  </td>
                  <td>{{confirmByCountry.provinceState}}</td>
                  <td> {{zz[index]}}</td>
                  <td>{{confirmByCountry.recovered}}</td>
                  <td>{{confirmByCountry.deaths}}</td>
                  <td> {{confirmByCountry.confirmed - (confirmByCountry.recovered+confirmByCountry.deaths)}}</td>
                  <td> <span
                      class="tag is-success is-normal">{{((confirmByCountry.recovered/confirmByCountry.confirmed)*100).toFixed(2)}}
                      %</span></td>
                  <td> <span
                      class="tag is-danger is-normal">{{((confirmByCountry.deaths/confirmByCountry.confirmed)*100).toFixed(3)}}
                      %</span></td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>



    </div>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        confirmed: '',
        recovered: '',
        percentageRecovered: '',
        deaths: '',
        percentageDeaths: '',
        treated: '',
        percentageTreated: '',
        date: '',
        lastUpdate: '',
        confirmByCountries: '',
        recoveredByCountries: '',
        deathByCountries: '',


        arrConfirmPercentage: [],
        zz: [],
        arrRecoveredPercentage: [],
        arrDeathPercentage: [],

        hasilDataMap: [],
     
        dataMaps: '',

        title: '',
        lat: '',
        long: '',
        xx: [],
        dataobj:''




      };
    },

    mounted() {
      this.getData();
      this.getDate();
      this.getConfirmbyCountry();
      this.getRecoveredbyCountry();
      this.getDeathbyCountry();
       this.dataForChart()
      this.barchart();
     
    },




    methods: {
      getData() {
        this.$axios.get('https://covid19.mathdro.id/api')
          .then(response => {
            this.lastUpdate = response.data.lastUpdate

            this.confirmedRaw = response.data.confirmed.value
            this.confirmed = Number(this.confirmedRaw).toLocaleString()

            this.recoveredRaw = response.data.recovered.value
            this.recovered = Number(this.recoveredRaw).toLocaleString()

            this.percentageRecoveredRaw = (this.recoveredRaw / this.confirmedRaw) * 100
            this.percentageRecovered = Math.round(this.percentageRecoveredRaw * 100) / 100

            this.deathsRaw = response.data.deaths.value
            this.deaths = Number(this.deathsRaw).toLocaleString()

            this.percentageDeathsRaw = (this.deathsRaw / this.confirmedRaw) * 100
            this.percentageDeaths = Math.round(this.percentageDeathsRaw * 100) / 100

            this.treatedRaw = this.confirmedRaw - (this.recoveredRaw + this.deathsRaw)
            this.treated = Number(this.treatedRaw).toLocaleString()

            this.percentagetreatedRaw = (this.treatedRaw / this.confirmedRaw) * 100
            this.percentageTreated = Math.round(this.percentagetreatedRaw * 100) / 100
          })
          .catch(e => {
            console.log(e)
          });
      },

      getConfirmbyCountry() {
        this.$axios.get('https://covid19.mathdro.id/api/confirmed')
          .then(response => {
            this.confirmByCountries = response.data
            // console.log('OOSMDDN' + this.confirmByCountries)
            // console.log('dasdad' + this.confirmByCountries.length)
            let i = 0
            for (i; i < this.confirmByCountries.length; i++) {

              let z = this.confirmByCountries[i].confirmed


              let arrzz = Number(z).toLocaleString()
              this.zz.push(arrzz)
              let x = (this.confirmByCountries[i].confirmed / this.confirmedRaw) * 100
              let y = x.toFixed(4)
              this.arrConfirmPercentage.push(y)
            }
          })
          .catch(e => {
            console.log(e)
          });
      },


      getRecoveredbyCountry() {
        this.$axios.get('https://covid19.mathdro.id/api/recovered')
          .then(response => {
            this.recoveredByCountries = response.data
            // console.log(this.recoveredBycountries.length)
            let i = 0
            for (i; i < this.recoveredByCountries.length; i++) {
              // console.log('sdasa' + ' ' + this.recoveredByCountries[i].recovered)
              let x = (this.recoveredByCountries[i].recovered / this.recoveredRaw) * 100
              let y = x.toFixed(4)
              this.arrRecoveredPercentage.push(y)
            }
          })
          .catch(e => {
            console.log(e)
          });
      },

      getDeathbyCountry() {
        this.$axios.get('https://covid19.mathdro.id/api/deaths')
          .then(response => {
            this.deathByCountries = response.data
            // console.log(this.recoveredBycountries.length)
            let i = 0
            for (i; i < this.deathByCountries.length; i++) {
              // console.log('sdasa' + ' ' + this.deathByCountries[i].deaths)
              let x = (this.deathByCountries[i].deaths / this.deathsRaw) * 100
              let y = x.toFixed(4)
              this.arrDeathPercentage.push(y)
            }
          })
          .catch(e => {
            console.log(e)
          });
      },


      getDate() {
        let currentdate = new Date();

        function days() {
          let hariRaw = currentdate.getDay()
          if (hariRaw = 6) {
            return 'Saturday'
          }

        }

        this.date = days() + ' ' + currentdate.getDate() + "/" +
          (currentdate.getMonth() + 1) + "/" +
          currentdate.getFullYear() + " @ " +
          currentdate.getHours() + ":" +
          currentdate.getMinutes() + ":" +
          currentdate.getSeconds();
      },


      dataForChart() {

        //      let {
        //   am4core,
        //   am4charts,
        //   am4maps,
        //   am4themes_animated,
        //   am4geodata_worldLow,
        //   am4themes_dark,

        // } = this.$am4core();
       
        this.$axios.get('https://covid19.mathdro.id/api/confirmed')
          .then(response => {
            this.dataMaps = response.data
            // this.databgst = this.dataMaps[i]
            // this.lat = this.dataMaps[i].lat;
            // this.long = this.this.dataMaps[i].long;
            // console.log('data map-> ' + this.dataMaps)

            //  let colorSet = new am4core.ColorSet();

            for (let i = 0; i < this.dataMaps.length; i++) {
              // console.log( this.dataMaps.length)
              // console.log([i])
              // console.log('sadadadaadadsd' + this.dataMaps[i].long)

               this.dataobj = {
                "title": this.dataMaps[i].countryRegion +' ' + this.dataMaps[i].provinceState,
                "latitude": this.dataMaps[i].lat,
                "longitude": this.dataMaps[i].long,
                // "color": colorSet.next(),
              }
               this.xx.push(this.dataobj)
              // this.res.push(dataobj)
              //  this.hasilDataMap.push(this.xx)

              console.log(this.xx)

              //  return this.xx
            }
          })
          .catch(e => {
            console.log(e)
          });


      },

     



      barchart() {
        let {
          am4core,
          am4charts,
          am4maps,
          am4themes_animated,
          am4geodata_worldLow,
          am4themes_dark,

        } = this.$am4core();

        let chart = am4core.create(this.$refs.chartdiv, am4maps.MapChart);

        chart.geodata = am4geodata_worldLow;

        // Set projection
        chart.projection = new am4maps.projections.Miller();

        // Create map polygon series
        let polygonSeries = chart.series.push(new am4maps.MapPolygonSeries());

        // Exclude Antartica
        polygonSeries.exclude = ["AQ"];

        // Make map load polygon (like country names) data from GeoJSON
        polygonSeries.useGeodata = true;

        // Configure series
        let polygonTemplate = polygonSeries.mapPolygons.template;
        polygonTemplate.tooltipText = "{name}";
        polygonTemplate.polygon.fillOpacity = 0.6;


        // Create hover state and set alternative fill color
        let hs = polygonTemplate.states.create("hover");
        hs.properties.fill = chart.colors.getIndex(0);

        // Add image series
        let imageSeries = chart.series.push(new am4maps.MapImageSeries());
        imageSeries.mapImages.template.propertyFields.longitude = "longitude";
        imageSeries.mapImages.template.propertyFields.latitude = "latitude";
        imageSeries.mapImages.template.tooltipText = "{title}";
        imageSeries.mapImages.template.propertyFields.url = "url";

        let circle = imageSeries.mapImages.template.createChild(am4core.Circle);
        circle.radius = 3;
        circle.propertyFields.fill = "color";

        let circle2 = imageSeries.mapImages.template.createChild(am4core.Circle);
        circle2.radius = 3;
        circle2.propertyFields.fill = "color";

        circle2.events.on("inited", function (event) {
          animateBullet(event.target);
        })


        function animateBullet(circle) {
          let animation = circle.animate([{
            property: "scale",
            from: 1,
            to: 5
          }, {
            property: "opacity",
            from: 1,
            to: 0
          }], 1000, am4core.ease.circleOut);
          animation.events.on("animationended", function (event) {
            animateBullet(event.target.object);
          })
        }

        let colorSet = new am4core.ColorSet();

    

        imageSeries.data =  this.xx

        // imageSeries.data = [{
        //   "title": "Brussels",
        //   "latitude": 50.8371,
        //   "longitude": 4.3676,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Copenhagen",
        //   "latitude": 55.6763,
        //   "longitude": 12.5681,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Paris",
        //   "latitude": 48.8567,
        //   "longitude": 2.3510,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Reykjavik",
        //   "latitude": 64.1353,
        //   "longitude": -21.8952,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Moscow",
        //   "latitude": 55.7558,
        //   "longitude": 37.6176,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Madrid",
        //   "latitude": 40.4167,
        //   "longitude": -3.7033,
        //   "color": colorSet.next()
        // }, {
        //   "title": "London",
        //   "latitude": 51.5002,
        //   "longitude": -0.1262,
        //   "url": "http://www.google.co.uk",
        //   "color": colorSet.next()
        // }, {
        //   "title": "Peking",
        //   "latitude": 39.9056,
        //   "longitude": 116.3958,
        //   "color": colorSet.next()
        // }, {
        //   "title": "New Delhi",
        //   "latitude": 28.6353,
        //   "longitude": 77.2250,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Tokyo",
        //   "latitude": 35.6785,
        //   "longitude": 139.6823,
        //   "url": "http://www.google.co.jp",
        //   "color": colorSet.next()
        // }, {
        //   "title": "Ankara",
        //   "latitude": 39.9439,
        //   "longitude": 32.8560,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Buenos Aires",
        //   "latitude": -34.6118,
        //   "longitude": -58.4173,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Brasilia",
        //   "latitude": -15.7801,
        //   "longitude": -47.9292,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Ottawa",
        //   "latitude": 45.4235,
        //   "longitude": -75.6979,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Washington",
        //   "latitude": 38.8921,
        //   "longitude": -77.0241,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Kinshasa",
        //   "latitude": -4.3369,
        //   "longitude": 15.3271,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Cairo",
        //   "latitude": 30.0571,
        //   "longitude": 31.2272,
        //   "color": colorSet.next()
        // }, {
        //   "title": "Pretoria",
        //   "latitude": -25.7463,
        //   "longitude": 28.1876,
        //   "color": colorSet.next()
        // }];

      },

      beforeDestroy() {

        
        if (this.chart) {
          this.chart.dispose();
        }
      },
    }
  }

</script>


<style>
  .hello {
    width: 100%;
    height: 530px;
  }

</style>
