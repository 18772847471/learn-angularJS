#ʲô�ǿ�����

AngularJS����������AngularJSӦ�ó�������ݣ��ǳ����JavaScript����

ng-controllerָ�������������Ӧ�ó���������ģ�����ͬʱ������һ���µ��������������Ӧ��DOMԪ���ϡ�

��ν���������һ��ָ��Ӧ��ģ�͵Ķ������Ǳ��ʽ��ִ�л������������в�νṹ�������κ���Ӧ��DOM������һ���ģ��������ܼ�ر��ʽ�ʹ����¼����ҿ��ԴӸ�������̳����ԡ�

ÿһ��AngularJSӦ�ö���һ�����Եĸ������򡣵�Ҳ�����ж���������� һ��Ӧ�ÿ����ж����������Ϊ��һЩָ��������µ��������򣬵��������򱻴�����ʱ�����ǻᱻ��������������ӵ����������£���ʹ�����������һ������ӦDOM�ṹһ������״�ṹ��

#�������ϵ�����

�������Ǿ���ng-controllerָ��������һ���򵥵Ŀ��������壬������ʾ��

    <div ng-app="" ng-controller="MyController">
    
    ������һ�����֣�<input type="text" ng-model="person.name"> 
    
    Hello <span ng-bind="person.name"></span> 
    
    </div>    
    
    <script>
    function MyController($scope) {
       $scope.person = {
          name: "zhu"
       };
    }
    </script>
    
��������������ͨ��ng-controllerָ�����һ��JavaScript���� ���� MyController������name���ԣ�

���Ǿ������MyController������� ���� $scope��

$scope���ǰ�һ��DOMԪ�����ᵽ�������ϵĶ������ṩһ���󶨵�DOMԪ��(�Լ�����Ԫ��)�ϵ�ִ�������ġ���Ҳ��һ��JavaScript����ָ��Ӧ�ó����������ڵ�����HTMLԪ�غ�ִ�������ġ�

Ҫ��ȷ����һ��$scope�������Ǿ�Ҫ��DOMԪ�ذ���һ��controller����ʹ�õ���ng-controller ָ�����ԡ�

����$scope����ѭԭ�ͼ̳У�����ζ�����Ƕ��ܷ��ʸ�$scope��,���κ����Ժͷ��������AngularJS�ڵ�ǰ$scope���Ҳ������ͻᵽ��$scope��ȥ�ң�����ڸ�$scope��Ҳû�ҵ����ͻ�������ϻ��ݣ�һֱ��$rootScope�ϣ����$rootScope�������$scope������Ӧ�ź��� ng-appָ�����Ե��Ǹ�DOMԪ�أ�Ҳ����˵�������������DOM����ng-appָ���ĵط���

Ҳ����˵��ӵ����$scope�����ǾͿ��Բ������������κ�������Ҫ��ȡ�Ķ������ݡ�

#��������������������

    <div ng-app="" ng-controller="MyController">
         ����:
         <input type="text" ng-model="username">
         <button ng-click="sayHello()">���к�</button>
         <hr>
         {{greeting}}
    </div>
    
    <script>
    function MyController($scope) {
      $scope.username = 'zhu';
      $scope.sayHello = function() {
        $scope.greeting= 'Hello ' + $scope.username + '!';
      };
    }
    </script>
    
    
#ע������
- ��Ҫ��ͼȥ����controller,һ��������һ��ֻ����һС����ͼ
- ��Ҫ��controller�в���DOM���ⲻ�ǿ�������ְ����ָ���ְ��
- ��Ҫ��controller�������ݸ�ʽ����ng�кܺ��õĹ�����ʵ�ִ˹��ܡ�
- ��Ҫ��controller���������ݹ��˲�����ng��$filter����
- һ����˵��controller�ǲ��ụ����õģ����������Ľ�����ͨ���¼����еġ�
