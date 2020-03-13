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
          <nav class="breadcrumb" aria-label="breadcrumbs">
            <ul>
              <li><a href="../">Bulma</a></li>
              <li><a href="../">Templates</a></li>
              <li><a href="../">Examples</a></li>
              <li class="is-active"><a href="#" aria-current="page">Admin</a></li>
            </ul>
          </nav>
          <section class="hero is-info welcome is-small">
            <div class="hero-body">
              <div class="container">
                <h1 class="title">
                  Hello, Admin.
                </h1>
                <h2 class="subtitle">
                  I hope you are having a great day!
                </h2>
              </div>
            </div> 
          </section>
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
                 <p class="title has-text-success">{{recovered}} <span class="subtitle has-text-success"> ({{percentageRecovered}}%) </span></p> 
                  <p class="subtitle has-text-success">Recovered</p>
                </article>
              </div>
              <div class="tile is-parent">
                <article class="tile is-child box">
                  <p class="title has-text-danger">{{deaths}} <span class="subtitle has-text-danger"> ({{percentageDeaths}}%) </span> </p>
                  <p class="subtitle has-text-danger">Deaths</p>
                </article>
              </div>
              <div class="tile is-parent">
                <article class="tile is-child box">
                  <p class="title">{{treated}}  <span class="subtitle "> ({{percentageTreated}}%) </span></p>
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
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
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
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
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
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
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
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
                        <tr>
                          <td width="5%"><i class="fa fa-bell-o"></i></td>
                          <td>Lorum ipsum dolem aire</td>
                          <td class="level-right"><a class="button is-small is-primary" href="#">Action</a></td>
                        </tr>
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
    </div>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        confirmed: '',
        recovered: '',
        percentageRecovered:'',
        deaths: '',
        percentageDeaths:'',
        treated: '',
        percentageTreated: ''
      };
    },

    mounted() {
      this.getData();
    },

    methods: {
      getData() {
        this.$axios.get('https://covid19.mathdro.id/api')
          .then(response => {
            
           this.confirmedRaw =response.data.confirmed.value
           this.confirmed = Number(this.confirmedRaw).toLocaleString()
          
            this.recoveredRaw = response.data.recovered.value 
            this.recovered = Number(this.recoveredRaw).toLocaleString() 

            this.percentageRecoveredRaw = (this.recoveredRaw /this.confirmedRaw) * 100 
            this.percentageRecovered = Math.round(this.percentageRecoveredRaw *100) /100

            this.deathsRaw = response.data.deaths.value  
            this.deaths =  Number(this.deathsRaw).toLocaleString() 
            
            this.percentageDeathsRaw = (this.deathsRaw /this.confirmedRaw) * 100 
            this.percentageDeaths = Math.round(this.percentageDeathsRaw *100) /100

            this.treatedRaw = this.confirmedRaw - (this.recoveredRaw + this.deathsRaw)
            this.treated = Number(this.treatedRaw).toLocaleString() 

             this.percentagetreatedRaw = (this.treatedRaw /this.confirmedRaw) * 100 
            this.percentageTreated = Math.round(this.percentagetreatedRaw *100) /100
          })
          .catch(e => {
            console.log(e)
          });      
      },

      

      

    }
  }

</script>


<style>

</style>
