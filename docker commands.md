# its build dockerfile image
- docker build -t mynginximage .

# its run container already buileded image
- docker run --name mynginxcontainer --network host -d mynginximage

  
