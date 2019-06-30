FROM bayesimpact/react-base

WORKDIR /usr/app
RUN rm -rf * .babelrc
RUN git clone https://github.com/nkmakinen/fullstackopen2018_osa1.git /usr/app
RUN npm install

EXPOSE 3000

CMD ["npm", "start"]