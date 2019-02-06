<template>
    <div class="modal fade" id="create-user" tabindex="-1" role="dialog" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title">Create user</h5>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="modal-body">
                    <form>
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" class="form-control" id="name" placeholder="Name" />
                        </div>
                        <div class="form-group">
                            <label for="state">State</label>
                            <input type="text" class="form-control" id="state" placeholder="State" />
                        </div>
                        <div class="form-group">
                            <label for="zip">Zip</label>
                            <input type="text" class="form-control" id="zip" placeholder="Zip" />
                        </div>
                        <div class="form-group">
                            <label for="country">Country</label>
                            <input type="text" class="form-control" id="country" placeholder="Country" />
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-primary" data-dismiss="modal">Cancel</button>
                    <button type="button" class="btn btn-warning" onSubmit={this.handleCreateBlog}>CREATE</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

import { connect } from 'react-redux';

import { ACTIONS } from '../../modules/Action';

import { createUser } from './services/Userservice';

export default {
    name: 'CreateBlog',
    data: {
        user: null
    },
    computed: () => {
        users = createUser();
    },
    methods: {
        mapStateToProps = (state) => ({
            items: data.user
        }),
        mapDispatchToProps = (dispatch) => ({
            createUser: (item) => dispatch(ACTIONS.createUser(item))
        }),
        handleCreateUser = (event) => {
            if (data.user !== null) {
                createUser(data.user);
            };
            event.preventDefault();
        }
    }
}
</script>