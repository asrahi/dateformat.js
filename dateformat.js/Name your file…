/**
 * dateformat prototype
 *
 * @author ASRAHI <classe82@naver.com>
 * @date 2019-07-21
 * @version 1.0
 * @license MIT
 *
 * @param format 날짜 format
 * @param lang 언어(객체로 넘기면 할당)
 * @retrun 자료형 설명
**/

var dateformat_en = {
	monthNames:["January","February","March","April","May","June","July","August","September","October","November","December"],
	monthNamesShort:["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"],
	dayNames:["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"],
	dayNamesShort:["Sun","Mon","Tue","Wed","Thu","Fri","Sat"],
	timeNames: ['am','pm'],
	timeNamesUpper: ['AM','PM']
}

Date.prototype.format = function(format,lang) {
	if (!this.valueOf()) return '';

	var str = {
		monthNames: ['1월', '2월', '3월', '4월', '5월', '6월', '7월', '8월', '9월', '10월', '11월', '12월'],
		monthNamesShort: ['1월', '2월', '3월', '4월', '5월', '6월', '7월', '8월', '9월', '10월', '11월', '12월'],
		dayNames: ["일요일", "월요일", "화요일", "수요일", "목요일", "금요일", "토요일"],
		dayNamesShort: ['일', '월', '화', '수', '목', '금', '토'],
		timeNames: ['오전','오후'],
		timeNamesUpper: ['AM','PM']
	}
	if( typeof lang == 'object' ) str = lang;

	var _this = this;

	return format.replace(/(Y|y|F|M|m|n|d|j|D|l|w|a|A|g|G|h|H|i|s)/g, function($1) {
		switch ($1) {

			case "Y": return _this.getFullYear(); //연도 4자리
			case "y": return String(_this.getFullYear()).slice(-2); //연도 2자리

			case "F": return str.monthNames[_this.getMonth()]; //월 긴표현
			case "M": return str.monthNamesShort[_this.getMonth()]; //월 짧은 표현
			case "m": return ('00'+(_this.getMonth() + 1)).slice(-2); //0이붙는 월
			case "M": return _this.getMonth(); //0이 붙지 않는 월

			case "d": return ('00'+_this.getDate()).slice(-2); //0이 붙는 일
			case "j": return _this.getDate(); //0이 붙지 않는 일

			case "D": return str.dayNamesShort[_this.getDay()]; //요일 글자 축약 표현
			case "l": return str.dayNames[_this.getDay()]; //요일 글자 표현
			case "w": return _this.getDay(); //요일 숫자 표현 (0일요일, 6토요일)

			case "g": return (_this.getHours() == 12) ? 12 : _this.getHours() % 12; //0이 붙지 않는 12시간 형식 시
			case "G": return _this.getHours(); //0이 붙지 않는 24시간 형식 시
			case "h": return ('00'+(_this.getHours() == 12) ? '12' : _this.getHours() % 12).slice(-2); //0이 붙는 12시간 형식 시
			case "H": return ('00'+_this.getHours()).slice(-2); //0이 붙는 24시간 형식 시

			case "a": return _this.getHours() < 12 ? str.timeNames[0] : str.timeNames[1]; //오전과 오후 소문자
			case "A": return _this.getHours() < 12 ? str.timeNamesUpper[0] : str.timeNamesUpper[1]; //오전과 오후의 대문자

			case "i": return ('00'+_this.getMinutes()).slice(-2); //0이 붙는 분
			case "s": return ('00'+_this.getSeconds()).slice(-2); //0이 붙는 초

			default: return $1;
		}
	});
};
