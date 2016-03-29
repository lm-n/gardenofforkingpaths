# gardenofforkingpaths
This is a project I worked on during IM's Project Studio @NYUAD. More info here: https://github.com/NYUAD-IM/Project-Studio

My project is based on a short story by Jorge Luis Borges, here's a section of the story that should give you and idea of what it is about:

"The fame of Ts'ui Pên as a calligrapher had been justly won. I read, uncomprehendingly and with fervor, these words written with a minute brush by a man of my blood: I leave to the various futures (not to all) my garden of forking paths. Wordlessly, I returned the sheet. 

Albert continued: "Before unearthing this letter, I had questioned myself about the ways in which a book can be infinite. I could think of nothing other than a cyclic volume, a circular one. A book whose last page was identical with the first, a book which had the possibility of continuing indefinitely. I remembered too that night which is at the middle of the Thousand and One Nights when Scheherazade (through a magical oversight of the copyist) begins to relate word for word the story of the Thousand and One Nights, establishing the risk of coming once again to the night when she must repeat it, and thus on to infinity. I imagined as well a Platonic. hereditary work. transmitted from father to son, in which each new individual adds a chapter or corrects with pious care the pages of his elders. These conjectures diverted me; but none seemed to correspond, not even remotely, to the contradictory chapters of Ts'ui Pên. In the midst of this perplexity, I received from Oxford the manuscript you have examined. I lingered, naturally, on the sentence: I leave to the various futures (not to all) my garden of forking paths. Almost instantly, I understood: 'the garden of forking paths' was the chaotic novel; the phrase 'the various futures (not to all)' suggested to me the forking in time, not in space. A broad rereading of the work confirmed the theory. In all fictional works, each time a man is confronted with several alternatives, he chooses one and eliminates the others; in the fiction of Ts'ui Pên, he chooses-- simultaneously--all of them. He creates, in this way, diverse futures, diverse times which themselves also proliferate and fork. Here, then, is the explanation of the novel's contradictions. Fang, let us say, has a secret; a stranger calls at his door; Fang resolves to kill him. Naturally, there are several possible outcomes: Fang can kill the intruder, the intruder can kill Fang, they both can escape, they both can die, and so forth. In the work of Ts'ui Pên, all possible outcomes occur; each one is the point of departure for other forkings. Sometimes, the paths of this labyrinth converge: for example, you arrive at this house, but in one of the possible pasts you are my enemy, in another, my friend. If you will resign yourself to my incurable pronunciation, we shall read a few pages." 

I was interested in the idea of a garden, a material/physical space being made of text and how that would look in today's world. So I decided to approach the project by creating a garden, that like the one of the story is made of text(in my case code and the text of the story) and has infinite forking paths, where the user walks through time and not space. To achieve this I decided to use Unity3D and MaxMSP.

  1) I took the short story and separated it by parts of speech using rita.js 
  
  2) then in MaxMSP I created a generative text system that using the words of the short story and simple grammatical rules could generate new texts.
  
  3) I rendered the text using jit.gl.text3D
  
  4) sent the text rendered graphics to Unity3D through Syphon
  
  5) in Unity3D I built modular laberynth of interconnected concentric cricles, and used the graphics rendered in MaxMSP as a texture on the walls by using Syphon for Unity3D. I used a first person camera, and added sounds of nature and of Shanghai Divas Jazz to recreate the sounds described in the story. 
  
  Here's a link to a video of how the environment looked like: https://youtu.be/0lf0kIn7JAc
  
Most of the challenges I face were in regards to Syphon and being able to use Syphon for Unity. After trying --with the help of Scott Fitzgerald-- for several weeks to use the Max graphics as a texture in Unity. Then I read in a Unity3D forum that changing the version of OpenGL used in Unity could helped. Changed it and taraaaa! It worked! However, some of the renderings were upside down, because I didn't consider the fact that one side of each wall would render the text correctly while the other would do it upside down. Working on fixing that. Stay tuned! 
