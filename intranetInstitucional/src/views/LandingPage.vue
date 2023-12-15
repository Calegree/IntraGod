<script setup>
import Navbar from "../components/Navbar.vue";
import NewsCard from "../components/NewsCard.vue";

/*const handleDeleteNews = async () => {

  const confirmDelete = window.confirm(
    "¿Are you sure you want to delete this News?"
  );
  if (!confirmDelete) {
    return;
  }
  try {
    const response = await axios.delete(
      `http://localhost:8080/corazondelatorback/deleteBorrow/${props.borrow.id}`
    );
  } catch (error) {
    console.error(error);
  }
};*/


</script>

<template>
  <Navbar />
  <div class="PageContainer">
    <div class="PageTitleContainer">
        <div class="titleTextContainer"><h1>News</h1></div>
      
    </div>
    <div class="NewsListContainer">
        <button type="button" class="btn btn-success CreateButton">Create News</button>
      <div class="NewsCardContainer">
        <NewsCard
          class="NewsCard"
          :NewsDate="'12/12/2012'"
          :NewsDescription="'soy una descripcion'"
          :NewsTitle="'Soy Un Titulo'"
          :NewsImage="'https://s1.eestatic.com/2021/03/13/actualidad/565703484_175278407_1280x1706.jpg'"
        />
        <button type="button" class="btn btn-danger DeleteButton" @click="handleDeleteNews" >Delete News</button>
        <button type="button" class="btn btn-warning EditButton">Edit News</button>
      </div>
      
    </div>
  </div>
</template>

<style>
.CreateButton{
    position: relative;
    left: 30%
}
.DeleteButton{

}
.EditButton{

}

.NewsCardContainer{
    margin-top: 20px;
    padding: 20px;
    background-color: #0109FF;
    border-radius: 5px;
}
.NewsListContainer {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.NewsCard {
  margin-top: 30px;
}
.PageTitleContainer {
  margin-top: 30px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.titleTextContainer{
    color:white;
    background-color: #0109FF;
    padding: 2px;
    padding-left: 20px;
    padding-right: 20px;
    border-radius: 5px;
}
</style>
