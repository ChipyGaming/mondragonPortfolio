<template>
<div>


<section id="home" class="w3l-banner py-5">
    <div class="container">
        <div class="row align-items-center">
        </div>
    </div>
</section>

<section class="w3l-aboutblock1" id="about">
    <div class="midd-w3 py-5">
        <div class="container py-lg-5 py-md-3">
            <div class="row">
                <div class="col-lg-4">
                    <div class="position-relative">
                        <img :src="data.main.fullimage" alt="" class="radius-image img-fluid">
                    </div>
                </div>
                <div class="col-lg-8 mt-lg-0 mt-5">
                    <h5 class="title-small mb-2">{{data.main.designation}}</h5>
                    <h3 class="title-big">Miguel Guerra-Mondragon</h3>
                    <p class="mt-4">{{data.main.bio}}</p>
                    <div class="my-info mt-4">
                        <div class="single-info"><span>Name:</span>
                            <p>{{data.main.name}}</p>
                        </div>
                        <div class="single-info"><span>Age:</span>
                            <p>{{data.main.age}}</p>
                        </div>
                        <div class="single-info"><span>From:</span>
                            <p>{{data.main.address.city}}, {{data.main.address.state}}</p>
                        </div>
                        <div class="single-info"><span>Email:</span>
                            <p><a :href="data.main.email">{{data.main.email}}</a></p>
                        </div>
                    </div>
                    <div class="my-social mt-lg-5 mt-4">
                        <a :href="data.main.resumedownload" target="_blank" class="btn btn-style btn-primary">View CV</a>
                        <ul class="social m-0 p-0">
                            <li v-for="social in data.main.social" v-bind:key="social" >
                                <a :href="social.url" target="_blank"><span :class="social.className"></span></a>
                            </li>
                            
                          </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>



<section class="w3l-services">
    <div class="w3l-achievements py-5" id="services">
        <div class="container py-lg-5">
            <h5 class="title-small text-center">Education</h5>
            <h3 class="title-big text-center mb-sm-5 mb-4">Degrees and Certificates </h3>
            <div class="row">
                
                <div class="col-lg-6 item" v-for="education in data.resume.education" v-bind:key="education">
                    <div class="card">
                        <div class="box-wrap">
                            <div class="icon">
                                <span class="fa fa-graduation-cap"></span>
                            </div>
                            <h4>{{education.degree}}</h4>
                            <p>
                                School : {{education.school}}<br>
                                Graduated : {{education.graduated}}<br>
                                Description : {{education.description}}<br>
                            </p>
                        </div>
                    </div>
                </div>
               <div class="col-lg-6 item" v-for="certificate in data.resume.certificate" v-bind:key="certificate">
                    <div class="card">
                        <div class="box-wrap">
                            <div class="icon">
                                <span class="fa fa-certificate"></span>
                            </div>
                            <h4>{{certificate.degree}}</h4>
                            <p>
                                School : {{certificate.school}}<br>
                                Graduated : {{certificate.graduated}}<br>
                                Description : {{certificate.description}}<br>
                            </p>
                        </div>
                    </div>
                </div>
                

            </div>
        </div>
    </div>
</section>

<div id = "work" class="anchor"></div>
<section class="w3l-services">
    <div class="w3l-achievements py-5" id="services">
        <div class="container py-lg-5">
            <h5 class="title-small text-center">Work</h5>
            <h3 class="title-big text-center mb-sm-5 mb-4">Past and Current Employement</h3>
            <div class="row">
                
                <div class="col-lg-6 item" v-for="work in data.resume.work" v-bind:key="work">
                    <div class="card">
                        <div class="box-wrap">
                            <div class="icon">
                                <span class="fa fa-briefcase"></span>
                            </div>
                            <h4>{{work.title}}</h4>
                            <p>
                                Company : {{work.company}}<br>
                                Year : {{work.years}}<br>
                                Description : {{work.description}}<br>
                                Tech Stack : {{work.technologies}}<br>
                            </p>
                        </div>
                    </div>
                </div>

                <div class="col-lg-6 item" v-for="work2 in data.resume.work2" v-bind:key="work2">
                    <div class="card">
                        <div class="box-wrap">
                            <div class="icon">
                                <span class="fa fa-briefcase"></span>
                            </div>
                            <h4>{{work2.title}}</h4>
                            <p>
                                Company : {{work2.company}}<br>
                                Year : {{work2.years}}<br>
                                Description : {{work2.description}}<br>
                            </p>
                        </div>
                    </div>
                </div>

                <div class="col-lg-6 item" v-for="work3 in data.resume.work3" v-bind:key="work3">
                    <div class="card">
                        <div class="box-wrap">
                            <div class="icon">
                                <span class="fa fa-briefcase"></span>
                            </div>
                            <h4>{{work3.title}}</h4>
                            <p>
                                Company : {{work3.company}}<br>
                                Year : {{work3.years}}<br>
                                Description : {{work3.description}}<br>
                                Tech Stack : {{work3.technologies}}<br>
                            </p>
                        </div>
                    </div>
                </div>

                <div class="col-lg-6 item" v-for="work4 in data.resume.work4" v-bind:key="work4">
                    <div class="card">
                        <div class="box-wrap">
                            <div class="icon">
                                <span class="fa fa-briefcase"></span>
                            </div>
                            <h4>{{work4.title}}</h4>
                            <p>
                                Company : {{work4.company}}<br>
                                Year : {{work4.years}}<br>
                                Description : {{work4.description}}<br>
                            </p>
                        </div>
                    </div>
                </div>
                
                

                

            </div>
        </div>
    </div>
</section>

<div id = "projects" class="anchor"></div>
<section class="w3l-services ">
    <div class="blog py-5" id="services">
        <div class="container py-lg-5">
            <h5 class="title-small text-center">Projects list</h5>
            <h3 class="title-big text-center mb-sm-5 mb-4">Past Solo or Team Projects</h3>
            <div class="row">
                
                    
                    <div class="col-md-4 col-sm-12 col-xs-12" v-for="project in data.portfolio.projects" v-bind:key="project">
                        <div class="item">
                            <div class="card">
								<a :href="project.url" target="_blank">
                                <div class="box-wrap">
                                    <div class="icon">
                                        <span class="fa fa-pencil-square-o"></span>
                                    </div>
                                    <h4 class="number">{{project.no}}</h4>
                                    <h4><a >{{project.title}}</a></h4>
                                    <p>{{project.description}}</p>
                                    <br>
                                    <p>Tech Stack: {{project.technologies}}</p>
                                </div>
								</a>
                            </div>
                        </div>
                    </div>
                    

            </div>
            <div class="mt-5 text-more">
                <p class="mt-4 pt-3 sample text-center">
                    
                </p>
            </div>
        </div>
    </div>
</section>


<div id = "contact" class="anchor"></div>
<section class="w3l-contact-1 py-5">
    <h5 class="title-small text-center">Contact Me</h5>
    <h3 class="title-big text-center mb-sm-5 mb-4">Usually available within 24 hours!</h3>
    <div class="contacts-9 py-lg-5 py-md-4">
        <div class="container">
            <div class="d-grid contact-view">
                <div class="cont-details">
                    <div class="cont-top">
                        <div class="cont-left text-center">
                            <span class="fa fa-phone text-primary"></span>
                        </div>
                        <div class="cont-right">
                            <h6>Call Me</h6>
                            <p><a :href="'tel:'+data.main.phone">{{data.main.phone}}</a></p>
                        </div>
                    </div>
                    <div class="cont-top margin-up">
                        <div class="cont-left text-center">
                            <span class="fa fa-envelope-o text-primary"></span>
                        </div>
                        <div class="cont-right">
                            <h6>Email Me</h6>
                            <p><a :href="'mailto:'+data.main.email" class="mail">{{data.main.email}}</a></p>
                        </div>
                    </div>
                    <div class="cont-top margin-up">
                        <div class="cont-left text-center">
                            <span class="fa fa-map-marker text-primary"></span>
                        </div>
                        <div class="cont-right">
                            <h6>Location</h6>
                            <p>{{data.main.address.street}}{{data.main.address.city}}, {{data.main.address.state}}, {{data.main.address.zip}}.</p>
                        </div>
                    </div>
                </div>
                <div class="map-content-9">
                    <div class="cont-top" v-for="social in data.main.social" v-bind:key="social">
                        <div class="cont-left text-center">
                            <span :class="social.className"></span>
                        </div>
                        <div class="cont-right">
                            <h6>{{social.name}}</h6>
                            <p><a :href="social.url"><font size="2px">{{social.url}}</font></a></p>
                        </div>
                    </div>
                   
                </div>
            </div>
        </div>
    </div>
</section>








</div>
</template>

<script>
import data from '~/static/api/data.json'
export default {
    
    name:"index",
    data(){
        return {
            data:data,
			
        }
    },
    head() {
      return {
        title: 'Home : '+this.data.main.name,
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'My custom description'
          }
        ]
      }
    }
}
</script>