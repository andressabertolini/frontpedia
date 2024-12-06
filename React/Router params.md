App.js
```
<Route path="/movie/:id" element={<MoviePage />} />
```

Movie component
```
<Link to={`/movie/${movie.ID}`}>
    Link
</Link>
```

Movie page
```
import { useParams } from 'react-router-dom';

const MoviePage = () => {
    const { id } = useParams();

    return <div className="movie-page">
        { id }
    </div>;
};

export default MoviePage;
```