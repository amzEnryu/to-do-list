<template>
    <div>
        <div class="d-flex justify-content-center mb-4">
            <div class="form-outline me-3" style="width: 14rem">
                <input type="text" id="form1" class="form-control" />
                <label class="form-label" for="form1">Example input</label>
            </div>
            <button type="button" class="btn btn-primary">Button</button>
        </div>

        <!-- Input group -->
        <div class="d-flex justify-content-center">
            <div class="input-group w-auto">
                <input type="text" class="form-control" placeholder="Example input" aria-label="Example input"
                    aria-describedby="button-addon1" />
                <button class="btn btn-primary" type="button" id="button-addon1" data-mdb-ripple-color="dark">
                    Button
                </button>
            </div>
        </div>
    </div>
</template>