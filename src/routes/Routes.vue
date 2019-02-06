<script>
import Vue from 'vue';
import VueRouter from 'vue-router';

Vue.use(VueRouter);

export default new Router({
    routes: [
        {
            path: '/',
            name: 'layout',
            component: Vue.component('Layout', require('../components/Layout.vue')),
            children: [
                {
                    path: 'about',
                    name: 'about',
                    component: Vue.component('About', require('../components/About.vue'))
                },
                {
                    path: 'contact',
                    name: 'contact',
                    component: Vue.component('Contact', require('../components/Contact.vue'))
                }
                {
                    path: 'displayusers',
                    name: 'displayusers',
                    component: Vue.component('DisplayUsers', require('../components/DisplayUsers.vue'))
                },
                {
                    path: 'displayblogs',
                    name: 'displayblogs',
                    component: Vue.component('DisplayBlogs', require('../components/DisplayBlogs.vue'))
                },
                {
                    path: 'displayposts',
                    name: 'displayposts',
                    component: Vue.component('DisplayPosts', require('../components/DisplayPosts.vue'))
                },
                {
                    path: 'displaycomments',
                    name: 'displaycomments',
                    component: Vue.component('DisplayComments', require('../components/DisplayComments.vue'))
                },
                {
                    path: 'createuser',
                    name: 'createuser',
                    component: Vue.component('CreateUser', require('../components/CreateUser.vue'))
                },
                {
                    path: 'createblog',
                    name: 'createblog',
                    component: Vue.component('CreateBlog', require('../components/CreateBlog.vue'))
                },
                {
                    path: 'createpost',
                    name: 'createpost',
                    component: Vue.component('CreatePost', require('../components/CreatePost.vue'))
                },
                {
                    path: 'createcomment',
                    name: 'createcomment',
                    component: Vue.component('CreateComment', require('../components/CreateComment.vue'))
                },
                {
                    path: 'updateuser',
                    name: 'updateuser',
                    component: Vue.component('UpdateUser', require('../components/UpdateUser.vue'))
                },
                {
                    path: 'updateblog',
                    name: 'updateblog',
                    component: Vue.component('UpdateBlog', require('../components/UpdateBlog.vue'))
                },
                {
                    path: 'updatepost',
                    name: 'updatepost',
                    component: Vue.component('UpdatePost', require('../components/UpdatePost.vue'))
                },              
                {
                    path: 'updatecomment',
                    name: 'updatecomment',
                    component: Vue.component('UpdateComment', require('../components/UpdateComment.vue'))
                },
                {
                    path: 'deleteuser',
                    name: 'deleteuser',
                    component: Vue.component('DeleteUser', require('../components/DeleteUser.vue'))
                },
                {
                    path: 'deleteblog',
                    name: 'deleteblog',
                    component: Vue.component('DeleteBlog', require('../components/DeleteBlog.vue'))
                },
                {
                    path: 'deletepost',
                    name: 'deletepost',
                    component: Vue.component('DeletePost', require('../components/DeletePost.vue'))
                },
                {
                    path: 'deleteComment',
                    name: 'deleteComment',
                    component: Vue.component('DeleteComment', require('../components/DeleteComment.vue'))
                }                
            ]
        }
    ]
});
</script>

