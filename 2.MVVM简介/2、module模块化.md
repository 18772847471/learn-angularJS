#ģ��

һ���Ǵ�ģ�鿪ʼ��module��������,������Ԫ�ض�����module����.

module
config filter directive factory controller
routes service
provider
value

#ģ��֮��������� ����ע��
        
        // ���ݲ�����ֹһ��,�����½�ģ��;����������ģ�鲻��������ģ��
        var createModule = angular.module("myModule", []);
        
        // ֻ��һ������(ģ����),�����ȡģ��
        // ���ģ�鲻����,angular��ܻ����쳣
        var getModule = angular.module("myModule");
        
�ú����ȿ��Դ����µ�ģ�飬Ҳ���Ի�ȡ����ģ�飬�Ǵ������ǻ�ȡ��ͨ�������ĸ��������֡�

    angular.module(name, [requires], [configFn]);
    
    - name���ַ������ͣ�����ģ������ƣ�
    - requires���ַ��������飬�����ģ������������ģ���б��������������ģ�飬�ÿ����鼴�ɣ�
    - configFn�������Ը�ģ�����һЩ���á�
    
ģ����һЩ���ܵļ��ϣ�������������񡢹�������ָ�����Ԫ����ɵ����塣

