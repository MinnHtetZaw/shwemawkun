<template>
  <div class="row gx-5">
    <div class="col-6">
      <div class="accordion cus-accordion" id="preSchool">
        <div class="accordion-item mb-3">
          <h2 class="accordion-header" id="preSchoolHeading">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
              data-bs-target="#preSchoolContent" aria-expanded="false" aria-controls="preSchoolContent">
              pre-school
            </button>
          </h2>
          <div id="preSchoolContent" class="accordion-collapse collapse" aria-labelledby="preSchoolHeading">
            <div class="accordion-body bg-white">
              <div class="course-group row align-items-center">
                <div class="col-8">
                  <h4 class="course text-uppercase"> Nurse & PRE-KG</h4>
                </div>
                <div class="col-4">
                  <h4 class="price text-uppercase">190,000 MMK</h4>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="accordion-item mb-3">
          <h2 class="accordion-header" id="primarySchoolHeading">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
              data-bs-target="#primarySchoolContent" aria-expanded="false" aria-controls="primarySchoolContent">
              primary school
            </button>
          </h2>
          <div id="primarySchoolContent" class="accordion-collapse collapse" aria-labelledby="primarySchoolHeading">
            <div class="accordion-body bg-white">
              <div class="course-group">
                <div class="row align-items-center">
                  <div class="col-8">
                    <h4 class="course text-uppercase">Foundation / kg</h4>
                    <h4 class="course text-uppercase">pre-starter / level 1</h4>
                    <h4 class="course text-uppercase">starter / level 2</h4>
                  </div>
                  <div class="col-4">
                    <h4 class="price text-uppercase">250,000 MMK</h4>
                  </div>
                </div>
              </div>
              <div class="course-group">
                <div class="row align-items-center">
                  <div class="col-8">
                    <h4 class="course text-uppercase">Movers/ level 3</h4>
                    <h4 class="course text-uppercase">flyer/ level 4</h4>
                  </div>
                  <div class="col-4">
                    <h4 class="price text-uppercase">300,000 MMK</h4>
                  </div>
                </div>
              </div>
              <div class="course-group">
                <div class="row align-items-center">
                  <div class="col-8">
                    <h4 class="course text-uppercase">A2 key (ket foundation)/ level 5</h4>
                    <h4 class="course text-uppercase">A2 key (ket)/ level 6</h4>
                  </div>
                  <div class="col-4">
                    <h4 class="price text-uppercase">360,000 MMK</h4>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="accordion-item">
          <h2 class="accordion-header" id="secondarySchoolHeading">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
              data-bs-target="#secondarySchoolContent" aria-expanded="false" aria-controls="secondarySchoolContent">
              secondary school
            </button>
          </h2>
          <div id="secondarySchoolContent" class="accordion-collapse collapse" aria-labelledby="secondarySchoolHeading">
            <div class="accordion-body bg-white">
              <div class="course-group">
                <div class="row align-items-center">
                  <div class="col-8">
                    <h4 class="course text-uppercase">b1 prelimainary(pet foundation)/ level
                      7</h4>
                    <h4 class="course text-uppercase">b1 prelimainary(pet)/ level 8</h4>
                  </div>
                  <div class="col-4">
                    <h4 class="price text-uppercase">450,000 MMK</h4>
                  </div>
                </div>
              </div>
              <div class="course-group">
                <div class="row align-items-center">
                  <div class="col-8">
                    <h4 class="course text-uppercase">B2 first(fce foundation)/ level 9</h4>
                    <h4 class="course text-uppercase">c1 advanced/ level(cae foundation)
                    </h4>
                  </div>
                  <div class="col-4">
                    <h4 class="price text-uppercase">300,000 MMK</h4>
                  </div>
                </div>
              </div>
              <div class="course-group">
                <div class="row align-items-center">
                  <div class="col-8">
                    <h4 class="course text-uppercase">A2 key (ket foundation)/ level 5</h4>
                    <h4 class="course text-uppercase">A2 key (ket)/ level 6</h4>
                  </div>
                  <div class="col-4">
                    <h4 class="price text-uppercase">360,000 MMK</h4>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- right side -->
    <div class="col-6">
      <div>
        <h5 class="mb-4 list">The following fees are not included in School Fees</h5>

        <ul>
          <li>Digital Resource and Teaching Aids</li>
          <li>Books</li>
          <li>School Uniform</li>
          <li>Materials & Lab Fees</li>
          <li>Certain Specialized Co-Curricular Activities</li>
        </ul>
      </div>
      <div class="image">

      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.image {
    background-position: bottom center;
    background-size: cover;
    background-repeat: no-repeat;
    background-image: url('@/assets/img/photo/06.png');
    height: 250px;
}

.cus-accordion {
    .accordion-item {
        border: 0;
    }

    .accordion-body {
        padding: 0;
        margin-top: -5px;
    }

    .accordion-button {
        text-transform: uppercase;
        font-weight: var(--cus-fw-semibold);
        background-color: var(--cus-primary);
        color: var(--cus-white);
        font-size: var(--fs-xxx-large);
        border-radius: var(--cus-border-radius);
        position: relative;

        &.collapsed {
            border-radius: var(--cus-border-radius);
        }

        &::after {
            color: var(--cus-white) !important;
            // chevron down icon from bootstrap
            background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16' fill='%23fff'%3e%3cpath fill-rule='evenodd' d='M1.646 4.646a.5.5 0 0 1 .708 0L8 10.293l5.646-5.647a.5.5 0 0 1 .708.708l-6 6a.5.5 0 0 1-.708 0l-6-6a.5.5 0 0 1 0-.708z'/%3e%3c/svg%3e");
            background-size: 3rem 3rem;
            width: 3rem;
            height: 3rem;
            position: absolute;
            top: 50%;
            right: 2%;
            transform: translateY(-50%) rotate(180deg);
        }

        &:not(.collapsed)::after {
            transform: translateY(-50%);
        }
    }

    .accordion-collapse {
        width: 95%;
        margin: 0 auto;
        border: 2px solid var(--cus-primary);
        border-radius: 0;
    }
}

.list {
    font-weight: var(--cus-fw-semibold);
}

.price {
    // white-space: nowrap;
    font-weight: var(--cus-fw-semibold);
}

.course {
    font-weight: var(--cus-fw-semibold);

    &:not(:last-child) {
        margin-bottom: 1.5rem;
    }
}

.course-group {
    padding: 1rem;

    &:not(:last-child) {
        border-bottom: 3px solid var(--cus-primary);
    }
}
</style>