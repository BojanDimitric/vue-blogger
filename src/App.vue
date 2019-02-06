<template>
    <ReduxProvider store={reduxStore}>
        <div id="app">        
            <Header />
            <Slider />
            <Layout />
            <Footer />
        </div>
    </ReduxProvider>
</template>

<script>
import Vue from 'vue';

import { Privider as ReduxProvider } from 'react-redux';
import  { configureStore } from '../modules/Store';

import Header from './components/Header';
import Slider from './components/Slider';
import Layout from './components/Layout';
import Footer from './components/Footer';

import About from './About';
import Contact from './Contact';

import DisplayUsers from './components/DisplayUsers';
import CreateUser from './components/CreateUser';
import UpdateUser from './components/UpdateUser';
import DeleteUser from './components/DeleteUser';
import DisplayBlog from './components/DisplayBlog';
import CreateBlog from './components/CreateBlog';
import UpdateBlog from './components/UpdateBlog';
import DeleteBlog from './components/DeleteBlog';
import DisplayPost from './components/DisplayPost';
import CreatePost from './components/CreatePost';
import UpdatePost from './components/UpdatePost';
import DeletePost from './components/DeletePost';
import DisplayComment from './components/DisplayComment';
import CreateComment from './components/CreateComment';
import UpdateComment from './components/UpdateComment';
import DeleteComment from './components/DeleteComment';

import BootstrapVue from 'bootstrap-vue';

import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap-vue/dist/bootstrap-vue.css';
import 'bootstrap/dist/js/bootstrap.js';

Vue.use(BootstrapVue);

export default {
    name: 'app',
    created: {
        reduxStore: configureStore(window.REDUX_INITIAL_DATA)
    },
    components: {
        Header,
        Slider,
        Layout,
        Footer,
        About,
        Contact,
        DisplayUsers,
        DisplayBlog,
        DisplayPost,
        DisplayComment,
        CreateUser,
        CreateBlog,
        CreatePost,
        CreateComment,
        DeleteUser,
        DeleteBlog,
        DeletePost,
        DeleteComment
    }
};
</script>
