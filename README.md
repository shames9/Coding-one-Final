# Coding-one-Final

As the course progressed into week 8, I was introduced to and learned about WebGL basic and the associated 3D geometry of 3D scenes, so I had the idea to build a cyberpunk city in js. As I really like a cyberpunk style, I tried to add more cyberpunk elements to the city, also inspired by 2077.

I learnt a lot from three.js about 3D models with different geometries and the rules and parameters of how they work in js. After setting up the language library and camera positions to accommodate the city, 
//var camera = new THREE.PerspectiveCamera(70, window.innerWidth / window.innerHeight, 1, 2500); 
I started to design and load each of the city buildings, the flying machines in the sky and the sky box as a background environment,//
//for (let i = 0; i < 6; i++)
      materialArray[i].side = THREE.BackSide;
    var skyBoxG = new THREE.BoxGeometry( 2000, 2000, 2000 );
      var skyBox = new THREE.Mesh (skyBoxG,materialArray);
      scene.add(skyBox);
I placed a cyberpunk feeling light source in the box to make the city look more cyberpunk
//var light = new THREE.DirectionalLight("rgb(182,59,151)");
After setting up the general location of the city buildings, I tried to add some pixel dots so that it would look like a fusion of starry sky and cyberpunk elements.
//for (var i = 0; i < 2000; i++) {
            var particle = new THREE.Vector3(
              (Math.random() - 0.5) * n,
              (Math.random() - 0.5) * n,
              (Math.random() - 0.5) * n
            );
            geom.vertices.push(particle);
            let color_k = Math.random();
            geom.colors.push(new THREE.Color(color_k, color_k, color_k * 2.0));
          }
Then I tried to make some of the buildings and flying machines rotate and self-pass to make the whole city work.
// torus.rotation.y+= 0.05;   
Autobiography of objects
// angle += 0.005;
   var x = 25 * Math.cos(angle);
   var y = 25 * Math.cos(angle);
   var z = 25 * Math.sin(angle);
  sphere.position.set(x/8-30,y+90,z*2);
Revolution of objects

By now the city was taking shape and I tried to add some cyberpunk style sounds by creating a maxiSample object using the parts of the sound I talked about in week two, loading two samples, using the maxiSample.play() function to manipulate the sound and triggering the per beat via maxiClock based on the BPM.
 // if (myClock.tick && myClock.playHead%64===0) {
            mySample.trigger();            
        }
unfortunately, my main audio file was corrupted and could not be recognised and uploaded to MIMIC, so only the secondary audio was used to form the background sound effects. In the rendering section I tried to render the whole city as a material or texture using a shader, but I couldn't do it, so I had to choose to use mapping to give the buildings a cyberpunk element.
//var myTexture20 = myTextureLoader20.load('building1.jpg');

When the whole project was completed, I felt that the scale of the city was not quite what I had expected. I had planned for the city to be about three times as big as it is now, but due to a lack of knowledge of architectural planning and a lack of time, I wasn't able to do a good job of representing the cyberpunk city I had in mind. The issue of sound has not been solved either, and I will study this knowledge in the following time and holidays to complete the whole city.

