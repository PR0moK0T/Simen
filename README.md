# Simen
const showInfo = (content) => {
    const lines = content.trim().split('\n');
  
    const dataLines = lines.slice(1); 

    const count = dataLines.length;
    console.log(`Count: ${count}`);
    
    
    const citylist = new Set()
    for (const line of dataLines) {
        const columns = line.split(',')
        const city = columns[7].trim()
        citylist.add(city)
    }
    const cityArr = Array.from(citylist).sort()
    console.log(`Cities: ${cityArr.join(', ')}`)

    const number = new Set()
    for (const line of dataLines) {
        const columns1 = line.split(',')
        const newNumber = columns1[3].trim()
        number.add(newNumber)
    }
    const numArr = Array.from(number).sort()
    console.log(`Humidity: Min: ${numArr[0]}, Max: ${numArr[numArr.length - 1]}`)
}

export default showInfo

Добавить в node в bin/weather.js __fixtures__/weather1.csv и bin/weather.js __fixtures__/weather2.csv
