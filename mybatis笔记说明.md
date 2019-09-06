# mybatis-
 <insert id="insertUser" parameterType="com.nuc.mybatis.po.User">
        <!--uuid()-->
        <!--
            <selectKey keyProperty="id" order="AFTER" resultType="java.lang.String">
              SELECT uuid()
            </selectKey>
            insert into user (id,username,birthday,sex,address) value(#{id},#{username},#{birthday},#{sex},#{address})
        -->
      <selectKey keyProperty="id" order="AFTER" resultType="java.lang.Integer">
          SELECT LAST_INSERT_ID()
      </selectKey>
      insert into user (username,birthday,sex,address) value(#{username},#{birthday},#{sex},#{address})
    </insert>
