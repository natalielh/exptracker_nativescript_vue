<template>
    <Page class="page">
        <ActionBar title="Simple Expense Tracker" class="action-bar" />

        <TabView height="100%">

            <!-- EXPENSES TAB -->
            <TabViewItem title="Expenses">
                <StackLayout orientation="vertical" width="100%" height="100%" class="main">
                    <Label text="Enter an expense:" textWrap="true" />
                    <TextField :text="textFieldValue" hint="expense" />
                    <Label text="Enter a cost:" textWrap="true" />
                    <TextField :text="textFieldValue" hint="$" />
                    <!-- Add New Expense button -->
					<Button text="Add New Expense" @tap="onButtonTap" />
                </StackLayout>
            </TabViewItem>

            <!-- INCOME TAB -->
            <TabViewItem title="Income">
                <StackLayout orientation="vertical" width="100%" height="100%" class="main">
					<Label text="Enter an income:" textWrap="true" />
					<TextField :text="textFieldValue" hint="income" />
					<Label text="Enter an amount:" textWrap="true" />
					<TextField :text="textFieldValue" hint="$" />
					<!-- Add New Income button -->
					<Button text="Add New Income" @tap="onButtonTap" />
                </StackLayout>
            </TabViewItem>

            <!-- TOTALS TAB -->
            <TabViewItem title="Totals">
                <StackLayout orientation="vertical" width="100%" height="100%" class="main">
					<Label text="You are currently spending $0" textWrap="true" />
					<Label text="You are currently making $0" textWrap="true" />
                </StackLayout>
            </TabViewItem>

        </TabView>
    </Page>
</template>

<script>
    export default {
        data() {
            return {};
        }
    };
</script>

<style scoped>
    .home-panel {
        vertical-align: center;
        font-size: 20;
        margin: 15;
    }

    .description-label {
        margin-bottom: 15;
    }

    .main {
        padding: 24;
    }
</style>