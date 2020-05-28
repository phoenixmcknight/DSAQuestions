# DSAQuestions
DSA Questions

//Create a function or method that when given a time (a string in HH:MM format) give this smallest angle created between the hour and minute hands. Please provide a https://repl.it/ link and a github


func clockAnglePracticeProblem(time:String) -> Int {
    
    let hourAndMinuteSeparated = time.components(separatedBy: ":")
    
    guard let hour = Int(hourAndMinuteSeparated[0]), let minute = Int(hourAndMinuteSeparated[1])  else {fatalError()}
    
    let minuteAngle = minute * 6
    
    let hourAngle = hour * 30 + (minute * 360) / (12 * 60)
    
    let calculatedClockAngle = abs(hourAngle - minuteAngle)
    
    return calculatedClockAngle > 180 ? 360 - calculatedClockAngle : calculatedClockAngle
}



