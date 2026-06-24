
<template>
  <div class="col-xl-12 col-md-12">
    <div class="row mt-2 mb-5 pb-3 mx-2">
      <div class="card card-body mb-5">

        <h2 class="main-title">
          Organizing Committee
        </h2>

        <div
          v-for="committee in committees"
          :key="committee.title"
          class="committee-section"
        >
          <h3 class="section-title">
            {{ committee.title }}
          </h3>

          <div class="committee-grid">
            <div
              v-for="member in committee.members"
              :key="member.name"
              class="member-card"
            >
              <img
                :src="getImage(member)"
                :alt="member.name"
                class="member-image"
              />

              <div class="member-content">
                <h5>{{ member.name }}</h5>
                <p>{{ member.organization }}</p>
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
  name: "Organising_Committee",

  data() {
    return {
      committees: [
        {
          title: "Chief Patron",
          members: [
            {
              name: "Prof. N. V. Ramana Rao",
              organization: "Director, NIT Raipur"
            }
          ]
        },

        {
          title: "Patron(s)",
          members: [
            {
              name: "Prof. Dr. Guru Prasad Subas Chandra Mishra",
              organization: "Dean (R&C), NIT Raipur"
            },
            {
              name: "Dr. Geetam Tomar",
              organization: "Chair IEEE Madhya Pradesh Section"
            },
            {
              name: "Shri. M K Badapanda",
              organization: "Chair IEEE PELS & IAS Madhya Pradesh Chapters"
            },
            {
              name: "Prof. Narendra D. Londhe",
              organization: "NIT Raipur"
            },
            {
              name: "Prof. S. Gupta",
              organization: "NIT Raipur"
            }
          ]
        },

        {
          title: "Honorary Chair",
          members: [
            {
              name: "Prof. Ashok Kumar Pradhan",
              organization: "IIT Kharagpur"
            },
            {
              name: "Prof. N. P. Padhy",
              organization: "MNIT Jaipur"
            },
            {
              name: "Prof. Nikos Hatziargyriou",
              organization: "NTUA, Greece"
            },
            {
              name: "Prof. Kashem Muttaqi",
              organization: "University of Wollongong, Australia"
            },
            {
              name: "Prof. Sanjib Panda",
              organization: "NUS Singapore"
            },
            {
              name: "Prof. Bijay Ketan Panigrahy",
              organization: "IIT Delhi"
            },
            {
              name: "Prof. Sukumar Mishra",
              organization: "IIT(ISM) Dhanbad"
            },
            {
              name: "Prof. Bidyadhar Subudhi",
              organization: "NIT Warangal"
            }
          ]
        },

        {
          title: "Industrial Chair",
          members: [
            {
              name: "Er. Hemant Verma",
              organization: "Tripura Electricity Regulatory Commission"
            }
          ]
        },

        {
          title: "General Chair / Chairperson",
          members: [
            {
              name: "Prof. Sachin Jain",
              organization: "HOD, Dept. of Electrical Engineering, NIT Raipur"
            }
          ]
        },

        {
          title: "Coordinators / Organizing Secretaries",
          members: [
            {
              name: "Dr. R. N. Patel",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Monalisa Biswal",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Surajit Sannigrahi",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Saurav Raj",
              organization: "NIT Raipur"
            }
          ]
        },

        {
          title: "Publication Chairs",
          members: [
            {
              name: "Prof. Swapnajit Pattnaik",
              organization: "NIT Raipur"
            },
            {
              name: "Prof. S. Ghosh",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Chilaka Ranga",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. B. Shaw",
              organization: "NIT Raipur"
            }
          ]
        },

        {
          title: "Publicity Chairs",
          members: [
            {
              name: "Prof. Archana Sharma",
              organization: "NIT Raipur"
            },
            {
              name: "Prof. Anamika Yadav",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Rajan Kumar",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. D. Suresh",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Jitendra Kumar",
              organization: "NIT Jamshedpur"
            },
            {
              name: "Dr. Gauri Shankar",
              organization: "IIT(ISM) Dhanbad"
            },
            {
              name: "Dr. Ashish Singhal",
              organization: "SGI Bhopal"
            },
            {
              name: "Dr. Dipanshu Naware",
              organization: "NIT Trichy"
            }
          ]
        },

        {
          title: "Finance Chair",
          members: [
            {
              name: "Dr. P. D. Dewangan",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Varsha Singh",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Ebha Koley",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Ramya Selvaraj",
              organization: "NIT Raipur"
            }
          ]
        },

        {
          title: "Track Chairs",
          members: [
            {
              name: "Dr. K. Chandrasekaran",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Hari Priya Vemuganti",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. B. N. Bag",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Sonti Venu",
              organization: "NIT Raipur"
            },
            {
              name: "Dr. Krishna Murari",
              organization: "IIT Bhilai"
            },
            {
              name: "Dr. Shashank Kurmi",
              organization: "IIT Bhilai"
            },
            {
              name: "Dr. Shailendra Kumar",
              organization: "IIT Bhilai"
            },
            {
              name: "Dr. Om Hari Gupta",
              organization: "NIT Jamshedpur"
            },
            {
              name: "Dr. Ravi Bhusan",
              organization: "NIT Jamshedpur"
            },
            {
              name: "Dr. Arpan Hota",
              organization: "IIT Kharagpur"
            },
            {
              name: "Dr. Satish Belkhode",
              organization: "IIT Roorkee"
            },
            {
              name: "Dr. Sateesh Kumar Kuncham",
              organization: "NIT Trichy"
            },
            {
              name: "Dr. Kiran Teeparthi",
              organization: "NIT AP"
            },
            {
              name: "Dr. Kotsampopoulos Panos",
              organization: "NTUA, Greece"
            },
            {
              name: "Dr. J. Ganesh",
              organization: "CEA, New Delhi"
            },
            {
              name: "Dr. Saumendra Sarangi",
              organization: "MNNIT Prayagraj"
            }
          ]
        }
      ]
    };
  },

  methods: {
    getImage(member) {
      try {
        return require(
          `@/committee_images/organising_committee/${member.name}, ${member.organization}.png`
        );
      } catch (error) {
        return "";
      }
    }
  }
};
</script>

<style scoped>
.main-title {
  text-align: center;
  font-weight: 700;
  margin-bottom: 40px;
  color: #1f2937;
}
.section-title {
  font-weight: 700;
  margin-bottom: 25px;
  color: #0f172a;
  text-align: center;
  padding-left: 0;
  border-left: none;
}
.committee-section {
  margin-bottom: 50px;
  text-align: center;
}
.committee-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 300px));
  gap: 24px;
  justify-content: center;
}

.member-card {
  background: #ffffff;
  border-radius: 18px;
  overflow: hidden;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.08);
  transition: all 0.35s ease;
  border: 1px solid rgba(0, 0, 0, 0.05);
}

.member-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 16px 35px rgba(0, 0, 0, 0.15);
}

.member-image {
  width: 100%;
  height: 280px;
  object-fit: contain;
  object-position: center;
  background: linear-gradient(135deg, #f8fafc, #e2e8f0);
  padding: 12px;
}

.member-content {
  padding: 18px;
  text-align: center;
}

.member-content h5 {
  font-size: 1rem;
  font-weight: 700;
  margin-bottom: 8px;
  color: #111827;
  line-height: 1.4;
}

.member-content p {
  margin: 0;
  color: #64748b;
  font-size: 0.9rem;
  line-height: 1.5;
}

@media (max-width: 992px) {
  .committee-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 576px) {
  .committee-grid {
    grid-template-columns: 1fr;
  }

  .member-image {
    height: 280px;
  }
}
</style>
```
