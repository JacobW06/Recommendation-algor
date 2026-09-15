I was dissatisfied with the how Spotify(and to an extent apple music) handled there recommendation algorithm. With that in mind, I set out to make a better one. 
This led me to the creation of this project. It draws parts of how Spotify runs there algorithm with some extra spice. Chiefly, I added more tags to the songs,
through the use of Ollama. This allows you to narrow your search down to specific genres and other things I thought were important 


PROBLEMS(ordered by importance)
1. Spotify subscription ran out. This means that some parts of the code are dependent on that. It still runs the cosine similarity on the songs, but it has to be
   queried correctly. Theoretically, it could be run without having to query Spotify's API at all. Just haven't got that far yet
2. Speed. This algorithm, with it's avoiding being rate limited, is very slow without the use of Ollama in the first place. Since Ollama has to tag every new song,
   it can really bog down the system. This is a hardware restriction, so it could be run on a cloud server that has better hardware than my laptop
3.Selection is spotty. Before getting to a "completed" point in the project, I was still using a API that was not fully complete. Spotify shut down there audio
   audio feature detection in late 2024. The API that I used is a digital clone from that time. Therefore, no new songs. As a backup for songs that are not on
   that digital clone, I am using a crowdsourced version that was discontinued in 2022. Since working on the project, I have discovered ways around these said
   problems but have yet to implement them.
