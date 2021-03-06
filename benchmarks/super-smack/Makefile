# Created by: Gea-Suan Lin <gslin@ccca.nctu.edu.tw>
# $FreeBSD$

PORTNAME=	super-smack
PORTVERSION=	1.3
PORTREVISION=	2
CATEGORIES=	benchmarks databases
MASTER_SITES=	GENTOO

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Benchmarking, stress testing, and load generation tool for Databases

GNU_CONFIGURE=	yes
CONFIGURE_ARGS+=	--with-smacks-dir=${DATADIR}
MAKE_JOBS_UNSAFE=	yes

PORTDOCS=	README TUTORIAL

OPTIONS_DEFINE=		DOCS
OPTIONS_MULTI=		DB
OPTIONS_MULTI_DB=	MYSQL PGSQL
OPTIONS_DEFAULT=	MYSQL

MYSQL_USE=		MYSQL=yes
MYSQL_CONFIGURE_ON=	--with-mysql \
			--with-mysql-include=${LOCALBASE}/include/mysql \
			--with-mysql-lib=${LOCALBASE}/lib/mysql

PGSQL_USES=		pgsql
PGSQL_CONFIGURE_ON=	--with-pgsql \
			--with-pgsql-include=${LOCALBASE}/include \
			--with-pgsql-lib=${LOCALBASE}/lib

post-install:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S|^|${WRKSRC}/|} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
