# Ruths.ai Coding Challenge

## Background  

Most old wells produce both and oil and gas mixture at the same time over the life of the well. The industry calls these production streams. The standard way to view this data is a line chart with multiple series (oil & gas over time).  

## User Story  

As an engineer, I am responsible for the production rates for multiple wells. I need to be able to visualize and monitor the production rates for each well over time.  

## Task  

Your challenge (if you choose to accept it :) is to create this data visualization using our API. Attached is an API response with 3 wells of production data. You can identify each well by the wellId. The wellId is a unique identifier for the well:  

`"wellId": "100041807911W600"`  

Each well has a series of data in the response object, we want to visualize each well’s oilRate and gasRate value over time. The user should be able to select a well, and see both production streams on a visualization. Then navigate to the next well, and so on.  

`"oilRate": {  
        "value": 0.73,  
        "uom": "m3/d"  
      }`  

## Requirements  

- The application should be built with [vue.js](https://vuejs.org) and use [Echarts](https://ecomfe.github.io/echarts-doc/public/en/index.html) using [Bootstrap v4](https://getbootstrap.com/) and [ES6](http://es6-features.org/#Constants) syntax  
- The implementation is due no later than 5pm CST on Friday March 1st, 2019 
- I should be able to review the project in GitHub  

### [Vue Guide](https://vuejs.org/v2/guide)  
### [Vue Style Guide](https://vuejs.org/v2/style-guide/)  
### [Bootstrap docs](https://getbootstrap.com/docs/4.3/getting-started/introduction)  

## Looking for  

- Production quality code  
- Responsive design principles  
- Comments where needed  
- Appropriate use of ES6 syntactic sugar  
- Clean visualizations  
- Reusable vue.js component architecture  

## Bonus  

- Aggregate statistics shown for each well (you can choose what to aggregate, e.g. sum of gas rate)  
- Hosted in the cloud (i.e. I can visit a URL and see the project)
- Project utilizes Ruths.ai logos and colors  

# streams

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
