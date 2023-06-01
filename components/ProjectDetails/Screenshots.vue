<template>
   <div class="container">
       <div class="container_desktop">
            <div class="single_card">
                <p class="single_card__description">If you played a role in the design or user interface aspect of the project, showcase your work in this section.</p>
                <div class="single_card__screenshot"></div>
            </div>
                      <div class="single_card">
                <p class="single_card__description">If you played a role in the design or user interface aspect of the project, showcase your work in this section.</p>
                <div class="single_card__screenshot"></div>
        </div>
       </div>
       <div class="container_mobile">
           <div class="container_mobile__img">imgs</div>
             <div class="container_mobile__img">imgs</div>
               <div class="container_mobile__img">imgs</div>
            
       </div>
   </div>
</template>


<style lang="scss" scoped>
@import "@/styles/variables.scss";


.container {
    margin: 5rem 0;
}

.container_desktop,
.container_mobile {
    display: flex;
    flex-direction: column;
    align-items: center;

}
.container_mobile {
    &__img {
        padding: 10rem 7rem;
        border: 1px solid black;
        margin: 1rem 0;
    }
}

.single_card {
    margin: 1rem;
    > * {
        margin: 1rem 0;
    }
    &__screenshot {
        width: inherit;
        height: 200px;
        border: 2px solid black;
    }
}

@media (min-width: 992px) {
    .container_desktop,
    .container_mobile {
        flex-direction: row;
        justify-content: space-around;
    }
}
</style>