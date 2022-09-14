# select base image 
FROM nginx

# label it
LABEL MAINTAIN=fahim@sparta

# copy data from localhost to the container
COPY index.html /usr/share/nginx/html/
COPY resume.css /usr/share/nginx/html/
COPY srt.png /usr/share/nginx/html/
COPY ttab.png /usr/share/nginx/html/
COPY __MACOSX /usr/share/nginx/html/

# allow required port 
EXPOSE 80

# execute required command
CMD ["nginx", "-g", "daemon off;"]