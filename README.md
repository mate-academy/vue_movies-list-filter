# Movies list - Filter

The `App` contains a search field and a list of movies. Implement filtering.

> Here is [the working version](https://mate-academy.github.io/vue_movies-list-filter/)

- Copy the `.movies` block from your solution of [Vue Movies List](https://github.com/mate-academy/vue_movies-list) to a `MovieList` component;
- move the `MovieSearch` to a separate component;
- implement `v-model` for `MovieSearch`;
- `query` should be stored in the `App` component;
- create a `visibleMovies` computed variable containing filtered movies;
- check if `movie.title` or `movie.description` contains `query`;
- ignore leading and trailing spaces;
- search should be case insensitive (`Inception` can be found by entering `inc` or `Inc` or even `iNC`).

## Instructions
- Install Prettier Extention and use this [VSCode settings](https://mate-academy.github.io/fe-program/tools/vscode/settings.json) to enable format on save.
- Open one more terminal and run tests with `npm test` to ensure your solution is correct.
- Replace `<your_account>` with your Github username in the [DEMO LINK](https://<your_account>.github.io/react_movies-list-js/) and add it to the PR description.
