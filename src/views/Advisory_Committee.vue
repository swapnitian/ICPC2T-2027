<template>
  <div class="col-xl-12 col-md-12">
    <div class="row mt-2 mb-5 pb-3 mx-2">
      <div class="card card-body mb-5">

        <h2 class="main-title">
          Advisory Board Members (Tentative)
        </h2>

        <!-- International Advisory Board -->
        <h3 class="section-title">
          International Advisory Board Members
        </h3>

        <div class="committee-grid">
          <div
            v-for="member in internationalMembers"
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

        <!-- National Advisory Board -->
        <h3 class="section-title mt-5">
          National Advisory Board Members
        </h3>

        <div class="committee-grid">
          <div
            v-for="member in nationalMembers"
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
</template>

<script>
export default {
  name: "Advisory_Committee",

  data() {
    return {
      internationalMembers: [
        {
          name: "Prof. Bikash Pal",
          organization: "Imperial College London"
        },
        {
          name: "Prof. Ayman El-Refaie",
          organization: "Marquette University, USA"
        },
        {
          name: "Prof. Sanjib Panda",
          organization: "National University of Singapore, Singapore"
        },
        {
          name: "Prof. Frede Blaabjerg",
          organization: "Aalborg University, Denmark"
        },
        {
          name: "Prof. Jih-Sheng (Jason) Lai",
          organization: "Virginia Tech, USA"
        },
        {
          name: "Prof. Akshay Rathore",
          organization: "National University of Singapore, Singapore"
        },
        {
          name: "Prof. Ramesh Bansal",
          organization: "University of Pretoria, South Africa"
        },
        {
          name: "Prof. Vinod Khadkikar",
          organization: "Khalifa University of Science & Technology, UAE"
        },
        {
          name: "Prof. Kashem Muttaqi",
          organization: "University of Wollongong, Australia"
        },
        {
          name: "Prof. Biplab Sikdar",
          organization: "National University of Singapore, Singapore"
        },
        {
          name: "Dr. Brij N. Singh",
          organization: "John Deere Inc, USA"
        }
      ],

      nationalMembers: [
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
        },
        {
          name: "Prof. Manisha Dubey",
          organization: "MANIT Bhopal"
        },
        {
          name: "Prof. Rajesh Kumar Nema",
          organization: "MANIT Bhopal"
        },
        {
          name: "Prof. Savita Nema",
          organization: "MANIT Bhopal"
        },
        {
          name: "Prof. Jyoti Singhi",
          organization: "MANIT Bhopal"
        },
        {
          name: "Prof. Ram Bilas Pachori",
          organization: "IIT Indore"
        },
        {
          name: "Prof. Kiran Kumar Pattanaik",
          organization: "IITM Gwalior"
        },
        {
          name: "Prof. Durgesh Kumar Mishra",
          organization: "SAIT Indore"
        },
        {
          name: "Prof. Sanjeev Singh",
          organization: "MANIT Bhopal"
        }
      ]
    };
  },

  methods: {
    getImage(member) {
      try {
        return require(
          `@/committee_images/advisory_committee/${member.name}, ${member.organization}.png`
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
  border-left: 5px solid #2563eb;
  padding-left: 12px;
}

.committee-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 24px;
}

.member-card {
  background: #ffffff;
  border-radius: 18px;
  overflow: hidden;
  box-shadow: 0 8px 25px rgba(0,0,0,0.08);
  transition: all 0.35s ease;
  border: 1px solid rgba(0,0,0,0.05);
}

.member-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 16px 35px rgba(0,0,0,0.15);
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