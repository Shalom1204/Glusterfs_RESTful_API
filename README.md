Glusterfs_restful API�ӿ�˵��
	��ϵͳ����java��JFinal���Ϊ����������ʵ�ֵ�һ��Glusterfs��һ��restful API��������Glusterfs���ػ���Զ�̣�ͨ��http����ķ�ʽ�����ƺͲ鿴glusterfs��Ⱥ�����ĵ�����glusterfs restful API�Ľӿ�ʹ��˵����
һ��	�����ļ�
���������ļ�λ����Դ��Ŀ¼��res�£����������������ļ���a_little_config.txt��log4j.properties������log4j.properties����־���ã�a_little_config.txt��ϵͳ���ò�����
����	������Ϣ��ʽ
Http����󷵻�һ��json��ʽ����İ����������Ķ�����Ҫ�����������֣�
i.	Obejct resultData����ʾ���صĽ������
ii.	Stack exceptionsStack ����ʾ�쳣��Ϣջ��������쳣�����쳣��Ϣ��ջ�С�
����	��Ⱥ��Ϣ
1.	��ȡ��Ⱥ��Ϣ
a)	gfs/getClusterInfo ��ȡ��Ⱥ������Ϣ���൱��gluster peer status����������ǰ��������Ľڵ㣬����Ⱥ�е����нڵ㣻gluster peer status����ʾ�����ڵ㣩�����ؽ����Map<String,String> ���У�key��ʾ�ڵ�ip��value��ʾ�ڵ��Ƿ�������ӣ�����PeerinCluster(Connected)��ʾ�������ӣ�PeerinCluster(DisConnected)��ʾ�������ӡ�
2.	���ü�Ⱥ
a)	gfs/probePeer/ip Ϊ��Ⱥ��ӽڵ㡣ͨ��url������Ҫ��ӵĽڵ���������ڵ�ip������ ��.�� �á�@�����Ŵ��档�൱��ִ��gluster peer probe������һ��������ʾ״̬������1��ʾ��ӳɹ���-1��ʾip���Ϸ���-2 ��ʾ����0��ʾ���ʧ�ܡ�
b)	gfs/detachPeer/ip Ϊ��Ⱥɾ���ڵ㡣ͨ��url������Ҫɾ���Ľڵ���������ڵ�ip������ ��.�� �á�@�����Ŵ��档�൱��ִ��gluster detach probe������һ��������ʾ״̬������1��ʾɾ���ɹ���-1��ʾip���Ϸ���-2 ��ʾ����0��ʾɾ��ʧ�ܡ�
�ġ�	���ݾ���Ϣ
a)	gfs/getAllVolumeInfo ��ȡ��Ⱥ����volume����Ϣ������һ��List<VolumeEntity>��VolumeEntity�а���һ��volume�Ļ�����Ϣ����������volume�����ݡ�
b)	gfs/getOneVolumeInfo ��ȡһ��volume����Ϣ��ͨ��url����һ��volumeName��Ȼ�󷵻�һ��VolumeEntity�Ķ��󣬵�������volume�����ݡ�
c)	gfs/getOneVolume/VolumeName ��ȡһ��volume������volume����Ϣ��volume�е����ݣ�����һ��VolumeEntity�Ķ���
d)	gfs/getAllVolume ��ȡ��Ⱥ����volume����Ϣ������һ��List<VolumeEntity>��VolumeEntity�а���һ��volume�Ļ�����Ϣ���Ұ���volume�����ݡ�
e)	gfs/stopVolume/volumeName ͨ��url����һ��volumeName��ֹͣVolumeName�ģ����أ�1 ��ʾ�ɹ� ��0��ʾ�Ѿ�����ֹͣ״̬��-1��ʾ volumeName�����ڣ�-2��ʾֹͣʧ�ܣ���������
f)	gfs/startVolume/volumeName ͨ��url����һ��volumeName����ʼVolumeName�ģ�����1 ��ʾ�ɹ� ��0��ʾ�Ѿ����ڿ�ʼ״̬��-1��ʾ volumeName�����ڣ�-2��ʾ��ʼʧ�ܣ���������
g)	gfs/createVolume/volumeName-count-type-bricks-moutPoint������bricks��~�ָ�,��ַ��.����@���棻����һ��״ֵ̬��0:�������ϸ� 1:���Դ��� ;-1��brick��ip���ڼ�Ⱥ�л���δ����;-2 -3 -4:��ʾ������brick��Ŀ��ƥ�� ; -5 :volumeName �Ѿ����ڣ�-6�����ص�����Ҳ�Ϊ�գ�������Ϊ���ص㡣
h)	gfs/deleteVolume/volumeName ͨ��url����һ��volumeName��ɾ��VolumeName�ģ�����1 ��ʾ�ɹ� ��-1��ʾvolume name�����ڣ�-2��ʾvolume ����ֹͣ״̬����ɾ����-3��ʾɾ��ʧ�ܣ�-4��ʾConstant.MountRecordPath�ļ�������;-5��ʾ��������
i)	VolumeEntity���������
 
�塢	���ݲ���
a)	data/removeData/pathɾ�����ݣ�ͨ��url������Ҫɾ���ļ������ļ��о���·��path������ɾ��path���񣬷���״ֵ̬��1��ʾ�������ɹ������������ɾ�������б�����ɾ����-1��ʾԴ�ļ������ڣ�����ɾ������
b)	data/copyData/sourcepath~destpath�������ݣ�ͨ��url������Ҫ�����ļ������ļ��о���·��sourcepath����Ҫ��������Ŀ��·��destpath����������path���񣬷���״ֵ̬��1��ʾ�������ɹ�����������뿽�������б����ڿ�����-1��ʾԴ�ļ������ڣ�������������
c)	data/ getOperateTasks ������ݲ��������б�����һ��List<TaskOperateData> operateDataTask������TaskOperateDataΪ�����࣬����ÿ�����ݲ���������Ҫ����Ϣ��
d)	TaskOperateData��������ԣ�
 
